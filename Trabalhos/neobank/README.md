# Atividade Prática – NeoBank+ (Ciclo Completo de Desenvolvimento)

Este repositório documenta o ciclo de desenvolvimento de software para a plataforma **NeoBank+**, um banco digital inteligente focado em pagamentos instantâneos, controle financeiro e segurança avançada.

O projeto foi desenvolvido como atividade prática da disciplina de Engenharia de Software, seguindo as 6 etapas do "Tema 6: Ciclo Completo de Desenvolvimento de Software".

## 🧭 Estrutura do Projeto (Artefatos Entregáveis)

[cite_start]Este repositório contém todos os artefatos exigidos como "Produto Final Esperado" , mapeados para as suas respectivas etapas de desenvolvimento:

| Etapa do Projeto | Artefato Entregável | Arquivo no Repositório |
| :--- | :--- | :--- |
| **Etapa 1:** Engenharia de Requisitos | Documento de Requisitos Priorizados | `./Requisitos.pdf` |
| **Etapa 2:** Desenho e Modelagem | Diagrama de Classes (MER) | `./Diagrama de Classes.pdf` |
| **Etapa 2:** Desenho e Modelagem | Protótipos de Interface (App Mobile) | `./Design Neobank+.pdf` |
| **Etapa 3:** Implementação (MVP) | MVP em Repositório (Web) | `./index.html`, `./style.css`, `./app.js` |
| **Etapa 4:** Testes | Plano de Testes com Evidências | `./Testes.pdf` |
| **Etapa 5:** Qualidade e Riscos | Relatório de Métricas e Riscos | *(Definido nesta documentação)* |
| **Etapa 6:** Reflexão Final | Reflexão Crítica | *(Definido nesta documentação)* |

---

## Etapa 1: Engenharia de Requisitos

A análise completa dos requisitos do sistema, conflitos e priorização está documentada no arquivo `Requisitos.pdf`.

[cite_start]Este documento inclui :
* **Requisitos Funcionais:** Detalhamento de 21 requisitos funcionais, como "Abertura de conta digital (KYC)", "Alertas de transações suspeitas" e "Gerenciamento de dispositivos conectados".
* **Requisitos Não Funcionais:** Definição de atributos de performance, segurança e conformidade, como "Escalabilidade para 5 milhões de contas", "Transações < 2 segundos" e "Conformidade com BACEN, LGPD".
* **Análise de Conflitos:** Mediação de conflitos clássicos como "Usabilidade vs. Segurança" (ex: "Tempo de login < 1 segundo" vs. "Autenticação em dois fatores") e "Rapidez vs. Conformidade" (ex: "Transações < 2s" vs. "Conformidade com BACEN").

## Etapa 2: Desenho e Modelagem

O design do sistema foi dividido em Modelagem de Dados e Prototipação de Interface.

* [cite_start]**Diagrama de Classes (MER):** O modelo lógico de dados está no arquivo `Diagrama de Classes.pdf` . Ele define as entidades centrais do sistema, seus atributos e métodos, como `Usuario`, `Cliente`, `Conta`, `Transacao`, `Cartao`, `Investimento`, `MetaFinanceira` e `LogAuditoria`.

* [cite_start]**Protótipos de Interface (App Mobile):** O arquivo `Design Neobank+.pdf`  [cite_start]contém os protótipos de alta fidelidade para o aplicativo mobile, conforme solicitado na Etapa 2 [cite: 778-781]. Este artefato visualiza o fluxo de usuário para as telas principais, incluindo:
    * [cite_start]Onboarding e Cadastro [cite: 8-42].
    * [cite_start]Login e Autenticação [cite: 43-60].
    * [cite_start]Dashboard (Home) [cite: 61-84].
    * [cite_start]Gerenciamento de Cartões (Físico e Virtual) [cite: 85-151].
    * [cite_start]Fluxo de Pagamento (Central Pix) [cite: 152-190].
    * [cite_start]Comprovantes de Transação [cite: 191-225].
    * [cite_start]Notificações e Estatísticas [cite: 226-275].

## Etapa 3: Implementação (MVP)

[cite_start]Esta pasta contém o MVP (Minimum Viable Product) funcional da interface web, implementado como uma SPA (Single Page Application) estática usando HTML, CSS e JavaScript, conforme os requisitos da Etapa 3 [cite: 782-787].

### Funcionalidades do MVP Implementadas

Este protótipo simula as seguintes funcionalidades essenciais:

1.  **Cadastro de Conta Digital Simples**
    * **Onde:** Página "Abrir Conta" (`#cadastro-page`).
    * **O que faz:** Um formulário (`form-cadastro`) que, ao ser enviado, exibe uma mensagem de sucesso (`#cadastro-success`) e redireciona o usuário para o Dashboard, simulando o fluxo em `app.js`.

2.  **Transferência PIX Mockada**
    * **Onde:** Página "PIX" (`#pix-page`).
    * **O que faz:** Permite o preenchimento de uma chave e valor (`form-pix`). Ao enviar, exibe uma mensagem de sucesso simulada (`#pix-success`).

3.  **Emissão de Cartão Virtual Mockado**
    * **Onde:** Página "Cartões" (`#cartoes-page`).
    * **O que faz:** Ao clicar no botão "Emitir Cartão Virtual" (`#btn-emitir-cartao`), um cartão virtual (`#cartao-virtual`) é exibido na tela.

4.  **Dashboard com Saldo e Extrato**
    * **Onde:** Página "Dashboard" (`#dashboard-page`).
    * **O que faz:** Exibe um saldo estático (`R$ 4.580,22`) e uma lista de transações recentes (`.extrato-lista`) com dados fixos.

5.  **Alerta de Transação Suspeita (Simulação)**
    * **Onde:** Página "Dashboard" (`#dashboard-page`).
    * **O que faz:** Um alerta de segurança estático (`#alerta-fraude`) é exibido no topo do dashboard, simulando o requisito funcional.

### README com Setup

#### Tecnologias Utilizadas
* **HTML5:** Estrutura semântica (`index.html`).
* **CSS3:** Estilização responsiva, Modo Escuro e Variáveis CSS (`style.css`).
* **JavaScript (ES6+):** Manipulação do DOM, navegação SPA e simulação de eventos (`app.js`).

#### Como Executar o Projeto
Como este projeto é um MVP estático (frontend puro), não há necessidade de compilação ou instalação de dependências.

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/gabriel-bcc/dce527/edit/main/Trabalhos/neobank
    ```

2.  **Abra o projeto:**
    * Navegue até a pasta do projeto (`cd neobank`).
    * Abra o arquivo `index.html` diretamente no seu navegador de preferência.

## Etapa 4: Testes

[cite_start]O plano de testes e as evidências de execução estão documentados em `Testes.pdf` . [cite_start]O documento detalha os cenários de teste para as funcionalidades exigidas [cite: 790-799], incluindo:

* [cite_start]**Caso 1:** Cadastro de conta válido [cite: 444-455].
* [cite_start]**Caso 2:** Transferência PIX bem-sucedida [cite: 456-470].
* [cite_start]**Caso 3:** Falha em transferência por saldo insuficiente [cite: 471-485].
* [cite_start]**Caso 4:** Emissão de cartão virtual [cite: 507-536].
* [cite_start]**Caso 5:** Registro de transação em extrato [cite: 537-542].
* [cite_start]**Caso 6:** Geração de relatório PDF [cite: 543-549].
* [cite_start]**Caso 7:** Alerta de fraude simulado [cite: 550-577].
* [cite_start]**Caso 8:** Teste de carga (100k transações) [cite: 578-681].
* [cite_start]**Caso 9:** Teste de segurança (Injeção SQL) [cite: 682-686].

## Etapa 5: Qualidade e Riscos

[cite_start]Esta seção define o "Relatório de Métricas e Riscos", conforme solicitado no `Tema 6.pdf` .

#### Métricas de Qualidade
* [cite_start]**Tempo de Resposta:** Todas as transações financeiras críticas devem ter tempo de resposta < 2 segundos[cite: 760].
* [cite_start]**Uptime (Disponibilidade):** O sistema deve manter 99,999% de disponibilidade[cite: 759].
* [cite_start]**Taxa de Fraude:** A meta é reduzir as fraudes em 40% (conforme `Tema 6.pdf` [cite: 767]).
* **Cobertura de Testes:** Garantir >90% de cobertura de testes unitários para os microserviços de Transação e Conta.

#### [cite_start]Análise de Riscos e Mitigação [cite: 802-807]
| Risco Identificado | Nível | Mitigação Proposta |
| :--- | :--- | :--- |
| **Ataques Cibernéticos (Phishing, DDoS)** | Alto | [cite_start]Implementar WAF (Web Application Firewall), monitoramento em tempo real (como o simulado no Caso 7 [cite: 550-577]) e treinamento de usuários. |
| **Vazamento de Dados Financeiros (LGPD)** | Alto | [cite_start]Criptografia de ponta a ponta [cite: 761] em todas as operações e em repouso. [cite_start]Auditoria e trilhas de log [cite: 762] para todas as transações. |
| **Indisponibilidade em Horários de Pico** | Médio | [cite_start]Arquitetura de microserviços em nuvem [cite: 775] com auto-scaling. [cite_start]Testes de carga (como o Caso 8 [cite: 578-681]) para identificar gargalos. |
| **Não Conformidade Regulatória (BACEN)** | Alto | Consultoria regulatória contínua. [cite_start]Garantir que todas as transações (PIX, TED) sigam as APIs oficiais [cite: 776] [cite_start]e regras de conformidade[cite: 761]. |

## Etapa 6: Reflexão Crítica

[cite_start]Esta seção aborda a "Reflexão Final", respondendo às questões propostas no `Tema 6.pdf` .

1.  **Como equilibrar usabilidade com segurança?**
    O equilíbrio é alcançado através da "autenticação adaptativa". O `Requisitos.pdf` sugere usar cache inteligente para dispositivos confiáveis (login rápido) e exigir 2FA (como biometria) apenas para ações sensíveis (como transferências altas ou visualização de dados detalhados), em vez de em cada login.

2.  **Quais trade-offs entre custo de infraestrutura e escalabilidade?**
    O principal trade-off é entre custo fixo (servidores dedicados) e custo variável (nuvem). [cite_start]A arquitetura de microserviços [cite: 775] [cite_start]é mais cara para iniciar (complexidade), mas oferece escalabilidade elástica (paga-se mais em horários de pico, mas economiza na baixa), o que é ideal para atingir 5 milhões de contas [cite: 758] sem superprovisionamento.

3.  **Como usar IA para reduzir fraudes sem prejudicar a experiência?**
    [cite_start]A IA (Machine Learning) [cite: 777] não deve bloquear transações suspeitas imediatamente (o que gera "falsos positivos" e frustra o usuário). Ela deve:
    * [cite_start]**Atuar em tempo real:** Analisar padrões (como no "Alerta de fraude simulado" [cite: 550-577]) e atribuir um "score de risco".
    * **Solicitar Verificação:** Para riscos médios, em vez de bloquear, o sistema pede uma segunda forma de autenticação (ex: biometria facial).
    * [cite_start]**Bloquear Apenas o Crítico:** O bloqueio automático (como no Caso 7 [cite: 568-569]) só ocorre em padrões de risco óbvios e muito altos (ex: "lavagem de centavos").

4.  **Quais desafios legais surgem ao operar em múltiplos países?**
    * **Conformidade de Dados:** Cada país tem sua própria LGPD (como o GDPR na Europa). A infraestrutura deve ser capaz de isolar dados de cidadãos por região.
    * **Conformidade Regulatória:** Cada país tem seu próprio "Banco Central" (BACEN) com regras diferentes para KYC, PIX (ou equivalentes) e combate à lavagem de dinheiro (AML).
    * **Linguagem:** O `Requisitos.pdf` nota que, mesmo com suporte multilingue, os documentos oficiais (extratos PDF) devem seguir o idioma oficial da regulação local (ex: Português no Brasil).

## 🌿 Estrutura de Branches (Repositório Git com branches organizadas)

[cite_start]Este repositório segue um modelo Git Flow simplificado para atender ao requisito de "branches organizadas":

* **`main`**: Branch principal. Contém apenas o código estável e entregável (versão final).
* **`develop`**: Branch de integração. Todo o desenvolvimento e novas funcionalidades são mesclados aqui antes de irem para a `main`.
* **`feature/*`**: Branches de funcionalidade (ex: `feature/pagina-pix`, `feature/dark-mode`). Elas são criadas a partir da `develop` e mescladas de volta na `develop` via Pull Request.
