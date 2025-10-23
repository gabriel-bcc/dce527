# Atividade Prática – NeoBank+ (Ciclo Completo de Desenvolvimento)

Este repositório documenta o ciclo de desenvolvimento de software para a plataforma **NeoBank+**, um banco digital inteligente focado em pagamentos instantâneos, controle financeiro e segurança avançada.

[cite_start]O projeto foi desenvolvido como atividade prática da disciplina de Engenharia de Software, seguindo as 6 etapas do "Tema 6: Ciclo Completo de Desenvolvimento de Software" [cite: 255-256].

## 🧭 Estrutura do Projeto (Artefatos Entregáveis)

[cite_start]Este repositório contém o código-fonte do MVP na raiz e todos os artefatos de documentação na pasta `/docs`, conforme os "Produtos Finais Esperados" [cite: 328-334].

| Etapa do Projeto | Artefato Entregável | Arquivo no Repositório |
| :--- | :--- | :--- |
| **Etapa 1:** Requisitos | Documento de Requisitos Priorizados | `./docs/Requisitos.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Casos de Uso | `./docs/Diagrama_Casos_de_Uso.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Classes (MER) | `./docs/Diagrama_de_Classes.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Arquitetura | *(Faltante - Arquitetura de Microserviços)* |
| **Etapa 2:** Modelagem | Protótipos de Interface (App Mobile) | `./docs/Design Neobank+.pdf` |
| **Etapa 3:** Implementação | MVP em Repositório (Web) | `./index.html`, `./style.css`, `./app.js` |
| **Etapa 4:** Testes | Plano de Testes com Evidências | `./docs/Testes.pdf` |
| **Etapa 5:** Qualidade | Relatório de Métricas e Riscos | *(Definido nesta documentação)* |
| **Etapa 6:** Reflexão | Reflexão Crítica | *(Definido nesta documentação)* |

---

## Etapa 1: Engenharia de Requisitos

[cite_start]A análise completa dos requisitos do sistema, conflitos e priorização está documentada no arquivo `docs/Requisitos.pdf` [cite: 1361-1395].

Este documento inclui:
* [cite_start]**Requisitos Funcionais:** Detalhamento de 21 requisitos funcionais, como "Abertura de conta digital (KYC)" [cite: 1363][cite_start], "Alertas de transações suspeitas em tempo real" [cite: 1367] [cite_start]e "Gerenciamento de dispositivos conectados" [cite: 1377-1378].
* [cite_start]**Requisitos Não Funcionais:** Definição de atributos de performance, segurança e conformidade, como "Escalabilidade para 5 milhões de contas ativas" [cite: 1386][cite_start], "Transações com tempo de resposta < 2 segundos" [cite: 275] [cite_start]e "Conformidade com BACEN, LGPD"[cite: 276].
* [cite_start]**Análise de Conflitos:** Mediação de conflitos clássicos como "Usabilidade vs. Segurança" e "Rapidez vs. Conformidade" [cite: 1392-1395].

## Etapa 2: Desenho e Modelagem

O design do sistema foi dividido em Modelagem de Dados e Prototipação de Interface.

* [cite_start]**Diagrama de Casos de Uso:** Detalha as interações dos atores "Cliente", "Administrador" e "Analista de Crédito" com o sistema[cite: 1321, 1322, 1323]. (Veja `docs/Diagrama_Casos_de_Uso.pdf`).
* **Diagrama de Classes (MER):** O modelo lógico de dados está no arquivo `docs/Diagrama_de_Classes.pdf`. Ele define as entidades centrais do sistema, como `Usuario`, `Cliente`, `Conta`, `Transacao` e `LogAuditoria`.
* [cite_start]**Protótipos de Interface (App Mobile):** O arquivo `docs/Design Neobank+.pdf` contém os protótipos de alta fidelidade para o aplicativo mobile [cite: 335-1253][cite_start], conforme solicitado na Etapa 2 [cite: 293-294]. Este artefato visualiza o fluxo de usuário para as telas principais, incluindo:
    * [cite_start]Onboarding e Cadastro [cite: 342-377, 802-837].
    * [cite_start]Login e Autenticação [cite: 380-396, 838-856].
    * [cite_start]Dashboard (Home) [cite: 397-420, 857-881].
    * [cite_start]Gerenciamento de Cartões (Físico e Virtual) [cite: 422-487, 882-950].
    * [cite_start]Fluxo de Pagamento (Central Pix) [cite: 488-542, 951-1003].
    * [cite_start]Comprovantes de Transação [cite: 543-577, 1004-1038].
    * [cite_start]Notificações e Estatísticas [cite: 578-627, 1039-1098].

## Etapa 3: Implementação (MVP)

[cite_start]O código-fonte na raiz deste repositório (`index.html`, `style.css`, `app.js`) constitui o MVP (Minimum Viable Product) funcional da interface web, conforme os requisitos da Etapa 3 [cite: 297-302].

### Funcionalidades do MVP Implementadas

Este protótipo simula as seguintes funcionalidades essenciais:

1.  [cite_start]**Cadastro de Conta Digital Simples** [cite: 298]
    * **Onde:** Página "Abrir Conta" (`#cadastro-page`).
    * **O que faz:** Um formulário (`form-cadastro`) que, ao ser enviado, exibe uma mensagem de sucesso (`#cadastro-success`) e redireciona o usuário para o Dashboard, simulando o fluxo em `app.js`.

2.  [cite_start]**Transferência PIX Mockada** [cite: 299]
    * **Onde:** Página "PIX" (`#pix-page`).
    * **O que faz:** Permite o preenchimento de uma chave e valor (`form-pix`). Ao enviar, exibe uma mensagem de sucesso simulada (`#pix-success`).

3.  [cite_start]**Emissão de Cartão Virtual Mockado** [cite: 300]
    * **Onde:** Página "Cartões" (`#cartoes-page`).
    * **O que faz:** Ao clicar no botão "Emitir Cartão Virtual" (`#btn-emitir-cartao`), um cartão virtual (`#cartao-virtual`) é exibido na tela.

4.  [cite_start]**Dashboard com Saldo e Extrato** [cite: 301]
    * **Onde:** Página "Dashboard" (`#dashboard-page`).
    * **O que faz:** Exibe um saldo estático (`R$ 4.580,22`) e uma lista de transações recentes (`.extrato-lista`) com dados fixos.

5.  [cite_start]**Alerta de Transação Suspeita (Simulação)** [cite: 302]
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
    git clone [URL-DO-SEU-REPOSITORIO]
    ```

2.  **Abra o projeto:**
    * Navegue até a pasta do projeto (ex: `cd neobank`).
    * Abra o arquivo `index.html` diretamente no seu navegador de preferência.

## Etapa 4: Testes

O plano de testes e as evidências de execução estão documentados em `docs/Testes.pdf`. [cite_start]O documento detalha os cenários de teste para as funcionalidades exigidas [cite: 305-314], incluindo:

* **Caso 1:** Cadastro de conta válido.
* **Caso 2:** Transferência PIX bem-sucedida.
* **Caso 3:** Falha em transferência por saldo insuficiente.
* **Caso 4:** Emissão de cartão virtual.
* **Caso 5:** Registro de transação em extrato.
* **Caso 6:** Geração de relatório PDF.
* **Caso 7:** Alerta de fraude simulado.
* **Caso 8:** Teste de carga (100k transações).
* **Caso 9:** Teste de segurança (Injeção SQL).

## Etapa 5: Qualidade e Riscos

[cite_start]Esta seção define o "Relatório de Métricas e Riscos", conforme solicitado [cite: 315-322, 333].

#### [cite_start]Métricas de Qualidade [cite: 316]
* [cite_start]**Tempo de Resposta:** Todas as transações financeiras críticas devem ter tempo de resposta < 2 segundos[cite: 275].
* [cite_start]**Uptime (Disponibilidade):** O sistema deve manter 99,999% de disponibilidade[cite: 274].
* [cite_start]**Taxa de Fraude:** A meta é reduzir as fraudes em 40%[cite: 282, 1397].
* **Cobertura de Testes:** Garantir >90% de cobertura de testes unitários para os microserviços de Transação e Conta.

#### [cite_start]Análise de Riscos e Mitigação [cite: 317-322]
| Risco Identificado | Nível | Mitigação Proposta |
| :--- | :--- | :--- |
| [cite_start]**Ataques Cibernéticos (Phishing, DDoS)** [cite: 318] | Alto | Implementar WAF (Web Application Firewall), monitoramento em tempo real (como o simulado no Caso 7) e treinamento de usuários. |
| [cite_start]**Vazamento de Dados Financeiros** [cite: 319] | Alto | [cite_start]Criptografia de ponta a ponta [cite: 276] e em repouso. [cite_start]Auditoria e trilhas de log para todas as transações[cite: 277]. |
| [cite_start]**Indisponibilidade em Horários de Pico** [cite: 320] | Médio | [cite_start]Arquitetura de microserviços em nuvem com auto-scaling[cite: 290]. Testes de carga (como o Caso 8) para identificar gargalos. |
| [cite_start]**Não Conformidade Regulatória (BACEN)** [cite: 321] | Alto | [cite_start]Consultoria regulatória contínua[cite: 322]. [cite_start]Garantir que todas as transações (PIX, TED) sigam as APIs oficiais e regras de conformidade[cite: 276]. |

## Etapa 6: Reflexão Crítica

[cite_start]Esta seção aborda a "Reflexão Final", respondendo às questões propostas [cite: 323-327, 334].

1.  [cite_start]**Como equilibrar usabilidade com segurança?** [cite: 324]
    O equilíbrio é alcançado através da "autenticação adaptativa". [cite_start]O `docs/Requisitos.pdf` sugere usar cache inteligente para dispositivos confiáveis (login rápido) e exigir 2FA (como biometria [cite: 1376][cite_start]) apenas para ações sensíveis (como transferências altas ou visualização de dados detalhados), em vez de em cada login[cite: 1392].

2.  [cite_start]**Quais trade-offs entre custo de infraestrutura e escalabilidade?** [cite: 325]
    O principal trade-off é entre custo fixo (servidores dedicados) e custo variável (nuvem). A arquitetura de microserviços [cite: 290] é mais cara para iniciar (complexidade), mas oferece escalabilidade elástica (paga-se mais em horários de pico, mas economiza na baixa), o que é ideal para atingir 5 milhões de contas [cite: 273, 1386] sem superprovisionamento.

3.  [cite_start]**Como usar IA para reduzir fraudes sem prejudicar a experiência?** [cite: 326]
    [cite_start]A IA (Machine Learning) [cite: 292] não deve bloquear transações suspeitas imediatamente (o que gera "falsos positivos" e frustra o usuário). Ela deve:
    * [cite_start]**Atuar em tempo real:** Analisar padrões (como no "Alerta de fraude simulado" [cite: 312]) e atribuir um "score de risco".
    * **Solicitar Verificação:** Para riscos médios, em vez de bloquear, o sistema pede uma segunda forma de autenticação (ex: biometria facial).
    * **Bloquear Apenas o Crítico:** O bloqueio automático (como no Caso 7) só ocorre em padrões de risco óbvios e muito altos (ex: "lavagem de centavos").

4.  [cite_start]**Quais desafios legais surgem ao operar em múltiplos países?** [cite: 327]
    * **Conformidade de Dados:** Cada país tem sua própria LGPD (como o GDPR na Europa). A infraestrutura deve ser capaz de isolar dados de cidadãos por região.
    * [cite_start]**Conformidade Regulatória:** Cada país tem seu próprio "Banco Central" (BACEN) com regras diferentes para KYC, PIX (ou equivalentes) e combate à lavagem de dinheiro (AML)[cite: 276].
    * [cite_start]**Linguagem:** O `docs/Requisitos.pdf` nota que, mesmo com suporte multilingue [cite: 1389][cite_start], os documentos oficiais (extratos PDF [cite: 270][cite_start]) devem seguir o idioma oficial da regulação local (ex: Português no Brasil)[cite: 1395].

## 🌿 Estrutura de Branches (Repositório Git com branches organizadas)

[cite_start]Este repositório segue um modelo Git Flow simplificado para atender ao requisito de "branches organizadas"[cite: 303]:

* **`main`**: Branch principal. Contém apenas o código estável e entregável (versão final).
* **`develop`**: Branch de integração. Todo o desenvolvimento e novas funcionalidades são mesclados aqui antes de irem para a `main`.
* **`feature/*`**: Branches de funcionalidade (ex: `feature/pagina-pix`, `feature/dark-mode`). Elas são criadas a partir da `develop` e mescladas de volta na `develop` via Pull Request.
