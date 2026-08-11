### Trabalho – Arquitetura e Soluções Cloud
## Alunos: Angely Munoz, Lucas Moro, Matheus Lucas da Silva, Erick Werner
# Definição do sistema — OrquestraCompras
O OrquestraCompras é uma plataforma web inteligente que auxilia usuários na busca e combinação de produtos disponíveis em diferentes lojas de e-commerce.
O usuário informa suas necessidades, preferências, orçamento disponível e lojas que deseja consultar. A partir dessas informações, o sistema utiliza agentes de Inteligência Artificial para pesquisar produtos nos e-commerces selecionados, analisar preços e características e gerar combinações de produtos adequadas aos critérios definidos pelo usuário.
A solução utiliza um modelo de linguagem (LLM) como apoio à interpretação das necessidades e análise das opções encontradas. O sistema também aplica regras de orçamento e restrições para selecionar e apresentar as melhores combinações ao usuário.
# Documentação de Arquitetura - OrquestraCompras

## Diagrama de Contexto (Nível 1)
O diagrama abaixo ilustra o contexto geral do sistema OrquestraCompras e suas interações com usuários e sistemas externos.

<img width="810" height="440" alt="Diagrama_1" src="https://github.com/user-attachments/assets/548b4aac-d1dc-4bc9-ac4b-9ae7ffcf1ccd" />

# Código
@startuml
skinparam defaultTextAlignment center
skinparam rectangle {
    BackgroundColor<<person>> #1168BD
    FontColor<<person>> #FFFFFF
    BackgroundColor<<system>> #08427B
    FontColor<<system>> #FFFFFF
    BackgroundColor<<external>> #999999
    FontColor<<external>> #FFFFFF
}

title Diagrama de Contexto (Nível 1) - OrquestraCompas

rectangle "Cliente / Usuário Final\n[Pessoa]" <<person>> as user
rectangle " OrquestraCompas\n[Sistema de Software]" <<system>> as matchmaker
rectangle "Sites de E-commerce Alvo\n[Sistema Externo]" <<external>> as ecommerce
rectangle "Provedor de LLM / IA\n[Sistema Externo]" <<external>> as ai_provider

user --> matchmaker : Configura o ambiente desejado, orçamento e lojas, e visualiza os combos\n[HTTPS / Web]
matchmaker --> ai_provider : Envia prompts e recebe análises estruturadas\n[API REST]
matchmaker --> ecommerce : Navega e extrai dados de produtos (preço, imagem, link)\n[HTTP / Scraping]

@enduml

## Diagrama de Containers (Nível 2)
O diagrama abaixo detalha os containers de software que compõem o sistema **OrquestraCompras**, dividindo a aplicação entre frontend, API de orquestração, workers assíncronos e camadas de persistência.

<img width="740" height="1365" alt="Diagrama 2" src="https://github.com/user-attachments/assets/4fa5e89c-d0cd-48ed-a254-5c69b2c5c4b1" />
 
### Descrição dos Containers

* **Aplicação Web (Next.js / React):** Interface de usuário responsável por coletar os critérios de busca e o orçamento do cliente, exibindo os resultados de forma interativa.
* **API de Orquestração (Python / FastAPI):** Ponto central de entrada do backend. Valida requisições, gerencia autenticação e enfileira as tarefas de busca.
* **Worker de Agentes IA (Python / Celery):** Motor de processamento em background responsável por executar a navegação inteligente, scraping e cruzamento de dados via LLM.
* **Fila de Tarefas (Redis):** Gerencia o fluxo de mensagens e tarefas assíncronas entre a API e os Workers.
* **Banco de Dados (PostgreSQL):** Armazena dados relacionais de usuários, histórico de buscas e os combos de produtos validados.

---

# Código Fonte (PlantUML)

plantuml
@startuml
skinparam defaultTextAlignment center
skinparam rectangle {
    BackgroundColor<<person>> #1168BD
    FontColor<<person>> #FFFFFF
    BackgroundColor<<system>> #08427B
    FontColor<<system>> #FFFFFF
    BackgroundColor<<container>> #1168BD
    FontColor<<container>> #FFFFFF
    BackgroundColor<<database>> #2E8B57
    FontColor<<database>> #FFFFFF
    BackgroundColor<<external>> #999999
    FontColor<<external>> #FFFFFF
}

title Diagrama de Containers (Nível 2) - OrquestraCompas

rectangle "Cliente\n[Pessoa]" <<person>> as user

rectangle " OrquestraCompas" {
    rectangle "Aplicação Web\n[Container: Next.js / React]" <<container>> as web_app
    rectangle "API de Orquestração\n[Container: Python / FastAPI]" <<container>> as api_gateway
    rectangle "Worker de Agentes IA\n[Container: Python / Celery]" <<container>> as worker
    rectangle "Banco de Dados\n[Container: PostgreSQL]" <<database>> as db
    rectangle "Fila de Tarefas\n[Container: Redis]" <<database>> as queue
}

rectangle "Sites de E-commerce\n[Sistema Externo]" <<external>> as ecommerce
rectangle "Provedor de LLM\n[Sistema Externo]" <<external>> as ai_provider

user --> web_app : Usa\n[HTTPS]
web_app --> api_gateway : Consome\n[JSON/HTTPS]
api_gateway --> db : Lê/Grava\n[SQL]
api_gateway --> queue : Envia tarefas\n[Redis Protocol]
queue --> worker : Processa\n[Redis Protocol]
worker --> ai_provider : Solicita inteligência\n[API REST]
worker --> ecommerce : Extrai dados\n[HTTP / Scraping]
worker --> db : Atualiza resultados\n[SQL]

@enduml

# Documentação de Arquitetura - OrquestraCompas

## Diagrama de Componentes (Nível 3)
O diagrama abaixo detalha os principais **componentes internos** que formam os containers de backend do sistema, especificando as responsabilidades da API de Orquestração e do Worker de Agentes IA.

![Uploading Diagrama 3.png…]()
 
#### 1. API de Orquestração (FastAPI)
* **AuthController:** Gerencia as rotas de autenticação, validando credenciais de usuários e emitindo tokens de acesso seguros.
* **SearchController:** Ponto de entrada que recebe a solicitação contendo os critérios da busca de produtos e o teto orçamentário.
* **TaskDispatcher:** Componente que empacota os parâmetros e despacha o job de forma assíncrona para a fila do Redis.

#### 2. Worker de Agentes IA (Celery)
* **AgentOrchestrator:** Cérebro do agente que gerencia o fluxo de raciocínio e o comportamento autônomo utilizando frameworks de IA.
* **ScraperEngine:** Utiliza automação de navegador (ex: Playwright) para extrair dados em tempo real dos e-commerces permitidos.
* **MatcherLogic:** Algoritmo responsável por cruzar as informações obtidas, validar restrições de preço e consolidar o combo perfeito para salvamento no banco de dados.

---

### Código Fonte (PlantUML)

plantuml
@startuml
skinparam defaultTextAlignment center
skinparam rectangle {
    BackgroundColor<<system>> #08427B
    FontColor<<system>> #FFFFFF
    BackgroundColor<<container>> #1168BD
    FontColor<<container>> #FFFFFF
    BackgroundColor<<component>> #85BB65
    FontColor<<component>> #FFFFFF
    BackgroundColor<<database>> #2E8B57
    FontColor<<database>> #FFFFFF
    BackgroundColor<<external>> #999999
    FontColor<<external>> #FFFFFF
}

title Diagrama de Componentes (Nível 3) - OrquestraCompas

rectangle "Aplicação Web\n[Container: Next.js / React]" <<container>> as web_app

rectangle "API de Orquestração (FastAPI)" {
    rectangle "AuthController\n[Component: FastAPI Router]" <<component>> as auth_controller
    rectangle "SearchController\n[Component: FastAPI Router]" <<component>> as search_controller
    rectangle "TaskDispatcher\n[Component: Celery Client]" <<component>> as task_dispatcher
}

rectangle "Worker de Agentes IA (Celery)" {
    rectangle "AgentOrchestrator\n[Component: Python / LangChain]" <<component>> as agent_orchestrator
    rectangle "ScraperEngine\n[Component: Playwright]" <<component>> as scraper_engine
    rectangle "MatcherLogic\n[Component: Python Algoritmo]" <<component>> as matcher_logic
}

rectangle "Fila de Tarefas\n[Container: Redis]" <<database>> as queue
rectangle "Banco de Dados\n[Container: PostgreSQL]" <<database>> as db

rectangle "Sites de E-commerce\n[Sistema Externo]" <<external>> as ecommerce
rectangle "Provedor de LLM\n[Sistema Externo]" <<external>> as ai_provider

web_app --> auth_controller : Autenticação\n[JSON/HTTPS]
web_app --> search_controller : Envia critérios de busca\n[JSON/HTTPS]
search_controller --> task_dispatcher : Dispara job\n[Python Code]
task_dispatcher --> queue : Enfileira tarefa\n[Redis Protocol]

queue --> agent_orchestrator : Consome tarefa\n[Redis Protocol]
agent_orchestrator --> scraper_engine : Comanda varredura\n[Python Code]
scraper_engine --> ecommerce : Extrai produtos\n[HTTP]
agent_orchestrator --> ai_provider : Interpreta HTML e valida combo\n[API REST]
agent_orchestrator --> matcher_logic : Aplica regras de orçamento\n[Python Code]
matcher_logic --> db : Salva combo final\n[SQL]

@enduml
