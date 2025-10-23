# Atividade Prática – NeoBank+ (Ciclo Completo de Desenvolvimento)

Este repositório documenta o ciclo de desenvolvimento de software para a plataforma **NeoBank+**, um banco digital inteligente focado em pagamentos instantâneos, controle financeiro e segurança avançada.

[cite_start]O projeto foi desenvolvido como atividade prática da disciplina de Engenharia de Software, seguindo as 6 etapas do "Tema 6: Ciclo Completo de Desenvolvimento de Software" [cite: 133-134, 156].

## 🧭 Estrutura do Projeto (Artefatos Entregáveis)

[cite_start]Este repositório contém o código-fonte do MVP na raiz e todos os artefatos de documentação na pasta `/docs`, conforme os "Produtos Finais Esperados" [cite: 206-212].

| Etapa do Projeto | Artefato Entregável | Arquivo no Repositório |
| :--- | :--- | :--- |
| **Etapa 1:** Requisitos | Documento de Requisitos Priorizados | `./docs/Requisitos.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Casos de Uso | `./docs/Diagrama de Caso de Uso.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Classes (MER) | `./docs/Diagramas de Classe UML Exemplo.pdf` |
| **Etapa 2:** Modelagem | Diagrama de Arquitetura | *(Faltante - Arquitetura de Microserviços)* |
| **Etapa 2:** Modelagem | Protótipos de Interface (App Mobile) | `./docs/Design Neobank+.pdf` |
| **Etapa 3:** Implementação | MVP em Repositório (Web) | `./index.html`, `./style.css`, `./app.js` |
| **Etapa 4:** Testes | Plano de Testes com Evidências | `./docs/Testes.pdf` |
| **Etapa 5:** Qualidade | Relatório de Métricas e Riscos | *(Definido nesta documentação)* |
| **Etapa 6:** Reflexão | Reflexão Crítica | *(Definido nesta documentação)* |

---

## Etapa 1: Engenharia de Requisitos

[cite_start]A análise completa dos requisitos do sistema, conflitos e priorização está documentada no arquivo `docs/Requisitos.pdf` [cite: 85-119].

Este documento inclui:
* [cite_start]**Requisitos Funcionais:** Detalhamento de 21 requisitos funcionais, como "Abertura de conta digital (KYC)" [cite: 87][cite_start], "Alertas de transações suspeitas em tempo real" [cite: 91] [cite_start]e "Gerenciamento de dispositivos conectados" [cite: 101-102].
* [cite_start]**Requisitos Não Funcionais:** Definição de atributos de performance, segurança e conformidade, como "Escalabilidade para 5 milhões de contas ativas" [cite: 110][cite_start], "Transações < 2 segundos" [cite: 122] [cite_start]e "Conformidade com BACEN, LGPD" [cite: 116-117].
* [cite_start]**Análise de Conflitos:** Mediação de conflitos clássicos como "Usabilidade vs. Segurança" e "Rapidez vs. Conformidade" [cite: 116-119].

## Etapa 2: Desenho e Modelagem

[cite_start]O design do sistema foi dividido em Modelagem de Dados e Prototipação de Interface, conforme solicitado [cite: 161-174].

* [cite_start]**Diagrama de Casos de Uso:** Detalha as interações dos atores "Cliente", "Administrador" e "Analista de Crédito" com o sistema . (Veja `docs/Diagrama de Caso de Uso.pdf`).
* [cite_start]**Diagrama de Classes (MER):** O modelo lógico de dados está no arquivo `docs/Diagramas de Classe UML Exemplo.pdf` [cite: 25-54]. [cite_start]Ele define as entidades centrais do sistema, como `Usuario` [cite: 30][cite_start], `Conta` [cite: 28][cite_start], `Transacao` [cite: 41] [cite_start]e `LogAuditoria`[cite: 53].
* [cite_start]**Protótipos de Interface (App Mobile):** O arquivo `docs/Design Neobank+.pdf` contém os protótipos de alta fidelidade para o aplicativo mobile [cite: 237-1155][cite_start], conforme solicitado [cite: 171-172]. Este artefato visualiza o fluxo de usuário para as telas principais, incluindo:
    * [cite_start]Onboarding e Cadastro [cite: 240-281, 699-739].
    * [cite_start]Login e Autenticação [cite: 282-298, 740-758].
    * [cite_start]Dashboard (Home) [cite: 299-322, 759-783].
    * [cite_start]Gerenciamento de Cartões (Físico e Virtual) [cite: 323-349, 784-810].
    * [cite_start]Fluxo de Pagamento (Central Pix) [cite: 390-444, 853-905].
    * [cite_start]Comprovantes de Transação [cite: 445-479, 906-940].
    * [cite_start]Notificações e Estatísticas [cite: 480-529, 941-1000].

## Etapa 3: Implementação (MVP)

[cite_start]O código-fonte na raiz deste repositório (`index.html`, `style.css`, `app.js`) constitui o MVP (Minimum Viable Product) funcional da interface web, conforme os requisitos da Etapa 3 [cite: 175-181].

### Funcionalidades do MVP Implementadas

Este protótipo simula as seguintes funcionalidades essenciais:

1.  [cite_start]**Cadastro de Conta Digital Simples** [cite: 176]
    * **Onde:** Página "Abrir Conta" (`#cadastro-page`).
    * **O que faz:** Um formulário (`form-cadastro`) que, ao ser enviado, exibe uma mensagem de sucesso (`#cadastro-success`) e redireciona o usuário para o Dashboard, simulando o fluxo em `app.js`.

2.  [cite_start]**Transferência PIX Mockada** [cite: 177]
    * **Onde:** Página "PIX" (`#pix-page`).
    * **O que faz:** Permite o preenchimento de uma chave e valor (`form-pix`). Ao enviar, exibe uma mensagem de sucesso simulada (`#pix-success`).

3.  [cite_start]**Emissão de Cartão Virtual Mockado** [cite: 178]
    * **Onde:** Página "Cartões" (`#cartoes-page`).
    * **O que faz:** Ao clicar no botão "Emitir Cartão Virtual" (`#btn-emitir-cartao`), um cartão virtual (`#cartao-virtual`) é exibido na tela.

4.  [cite_start]**Dashboard com Saldo e Extrato** [cite: 179]
    * **Onde:** Página "Dashboard" (`#dashboard-page`).
    * **O que faz:** Exibe um saldo estático (`R$ 4.580,22`) e uma lista de transações recentes (`.extrato-lista`) com dados fixos.

5.  [cite_start]**Alerta de Transação Suspeita (Simulação)** [cite: 180]
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
    git clone [https://github.com/gabriel-bcc/dce527/tree/main/Trabalhos/neobank](https://github.com/gabriel-bcc/dce527/tree/main/Trabalhos/neobank)
    ```

2.  **Abra o projeto:**
    * Navegue até a pasta do projeto (ex: `cd neobank`).
    * Abra o arquivo `index.html` diretamente no seu navegador de preferência.

## Etapa 4: Testes

O plano de testes e as evidências de execução estão documentados em `docs/Testes.pdf`. [cite_start]O documento detalha os cenários de teste para as funcionalidades exigidas [cite: 182-192], incluindo:

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

[cite_start]Esta seção define o "Relatório de Métricas e Riscos", conforme solicitado [cite: 193-200, 211].

#### Métricas de Qualidade
* [cite_start]**Tempo de Resposta:** Todas as transações financeiras críticas devem ter tempo de resposta < 2 segundos[cite: 122, 153].
* [cite_start]**Uptime (Disponibilidade):** O sistema deve manter 99,999% de disponibilidade[cite: 114, 152].
* [cite_start]**Taxa de Fraude:** A meta é reduzir as fraudes em 40%[cite: 121, 160].
* **Cobertura de Testes:** Garantir >90% de cobertura de testes unitários para os microserviços de Transação e Conta.

#### [cite_start]Análise de Riscos e Mitigação [cite: 195-200]
| Risco Identificado | Nível | Mitigação Proposta |
| :--- | :--- | :--- |
| **Ataques Cibernéticos (Phishing, DDoS)** | Alto | Implementar WAF (Web Application Firewall), monitoramento em tempo real (como o simulado no Caso 7) e treinamento de usuários. |
| **Vazamento de Dados Financeiros (LGPD)** | Alto | [cite_start]Criptografia de ponta a ponta [cite: 154] e em repouso. [cite_start]Auditoria e trilhas de log para todas as transações[cite: 155]. |
| **Indisponibilidade em Horários de Pico** | Médio | Arquitetura de microserviços em nuvem com auto-scaling. Testes de carga (como o Caso 8) para identificar gargalos. |
| **Não Conformidade Regulatória (BACEN)** | Alto | Consultoria regulatória contínua. [cite_start]Garantir que todas as transações (PIX, TED) sigam as APIs oficiais e regras de conformidade[cite: 154]. |

## Etapa 6: Reflexão Crítica

[cite_start]Esta seção aborda a "Reflexão Final", respondendo às questões propostas [cite: 201-205, 212].

1.  **Como equilibrar usabilidade com segurança?**
    O equilíbrio é alcançado através da "autenticação adaptativa". O `docs/Requisitos.pdf` sugere usar cache inteligente para dispositivos confiáveis (login rápido) e exigir 2FA (como biometria) apenas para ações sensíveis (como transferências altas ou visualização de dados detalhados), em vez de em cada login[cite: 116].

2.  **Quais trade-offs entre custo de infraestrutura e escalabilidade?**
    O principal trade-off é entre custo fixo (servidores dedicados) e custo variável (nuvem). A arquitetura de microserviços [cite: 167-168] é mais cara para iniciar (complexidade), mas oferece escalabilidade elástica (paga-se mais em horários de pico, mas economiza na baixa), o que é ideal para atingir 5 milhões de contas [cite: 110] sem superprovisionamento.

3.  **Como usar IA para reduzir fraudes sem prejudicar a experiência?**
    A IA (Machine Learning) [cite: 131, 170] não deve bloquear transações suspeitas imediatamente (o que gera "falsos positivos" e frustra o usuário). Ela deve:
    * **Atuar em tempo real:** Analisar padrões (como no "Alerta de fraude simulado") e atribuir um "score de risco".
    * **Solicitar Verificação:** Para riscos médios, em vez de bloquear, o sistema pede uma segunda forma de autenticação (ex: biometria facial)[cite: 100].
    * **Bloquear Apenas o Crítico:** O bloqueio automático (como no Caso 7) só ocorre em padrões de risco óbvios e muito altos (ex: "lavagem de centavos").

4.  **Quais desafios legais surgem ao operar em múltiplos países?**
    * **Conformidade de Dados:** Cada país tem sua própria LGPD (como o GDPR na Europa). A infraestrutura deve ser capaz de isolar dados de cidadãos por região.
    * [cite_start]**Conformidade Regulatória:** Cada país tem seu próprio "Banco Central" (BACEN) com regras diferentes para KYC, PIX (ou equivalentes) e combate à lavagem de dinheiro (AML)[cite: 154].
    * [cite_start]**Linguagem:** O `docs/Requisitos.pdf` nota que, mesmo com suporte multilingue [cite: 113][cite_start], os documentos oficiais (extratos PDF) devem seguir o idioma oficial da regulação local (ex: Português no Brasil)[cite: 119].

## 🌿 Estrutura de Branches (Repositório Git com branches organizadas)

[cite_start]Este repositório segue um modelo Git Flow simplificado para atender ao requisito de "branches organizadas"[cite: 181]:

* **`main`**: Branch principal. Contém apenas o código estável e entregável (versão final).
* **`develop`**: Branch de integração. Todo o desenvolvimento e novas funcionalidades são mesclados aqui antes de irem para a `main`.
* **`feature/*`**: Branches de funcionalidade (ex: `feature/pagina-pix`, `feature/dark-mode`). Elas são criadas a partir da `develop` e mescladas de volta na `develop` via Pull Request.
