# MVP NeoBank+

Este é o repositório do MVP (Minimum Viable Product) para o projeto NeoBank+, um banco digital inteligente[cite: 490]. [cite_start]Este projeto foi desenvolvido como parte da atividade acadêmica "Ciclo Completo de Desenvolvimento de Software" (Tema 6)[cite: 486, 487].

[cite_start]O foco deste MVP é demonstrar a interface do usuário (UI) e as interações *mockadas* (simuladas) das principais funcionalidades, conforme especificado nos requisitos de implementação da Etapa 3[cite: 528].

## 🚀 Funcionalidades do MVP Implementadas

Este protótipo é uma SPA (Single Page Application) estática que simula o fluxo de um banco digital. [cite_start]As seguintes funcionalidades do MVP estão presentes[cite: 528]:

1.  [cite_start]**Cadastro de Conta Digital Simples** [cite: 529]
    * **Onde:** Página "Abrir Conta".
    * **O que faz:** Um formulário de cadastro (`form-cadastro`) que, ao ser enviado, exibe uma mensagem de sucesso simulada (`cadastro-success`) e redireciona o usuário para o Dashboard.

2.  [cite_start]**Transferência PIX Mockada** [cite: 530]
    * **Onde:** Página "PIX".
    * **O que faz:** Permite o preenchimento de uma chave e valor (`form-pix`). Ao enviar, exibe uma mensagem de sucesso simulada (`pix-success`).

3.  [cite_start]**Emissão de Cartão Virtual Mockado** [cite: 531]
    * **Onde:** Página "Cartões".
    * **O que faz:** Ao clicar no botão "Emitir Cartão Virtual" (`btn-emitir-cartao`), um cartão virtual simulado (`cartao-virtual`) é exibido na tela.

4.  [cite_start]**Dashboard com Saldo e Extrato** [cite: 532]
    * **Onde:** Página "Dashboard".
    * **O que faz:** Exibe um saldo estático (`R$ 4.580,22`) e uma lista de transações recentes (extrato) com dados fixos.

5.  [cite_start]**Alerta de Transação Suspeita (Simulação)** [cite: 533]
    * **Onde:** Página "Dashboard".
    * [cite_start]**O que faz:** Um alerta de segurança estático (`alerta-fraude`) é exibido no topo do dashboard para simular a detecção de fraude[cite: 498].

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estrutura semântica do site (`index.html`).
* **CSS3:** Estilização completa, incluindo (`style.css`):
    * Design Responsivo.
    * Modo Escuro (Dark Mode) com `body.dark-mode`.
    * Variáveis CSS para gerenciamento de tema.
* **JavaScript (ES6+):** (`app.js`)
    * Manipulação do DOM.
    * Simulação de SPA (Single Page Application) para navegação sem recarregar a página.
    * Persistência do tema (Modo Escuro) usando `localStorage`.
    * Simulação de eventos de formulário (submit).

## ⚙️ Setup e Instalação (README com setup)

[cite_start]Como este projeto é um MVP estático (frontend puro) sem a necessidade de um backend ou compilação, o setup é muito simples[cite: 534]:

1.  **Clonar o repositório:**
    ```bash
    git clone https://github.com/gabriel-bcc/dce527/edit/main/Trabalhos/neobank.git
    ```

2.  **Abrir o projeto:**
    * Navegue até a pasta do projeto (`cd neobank-mvp`).
    * Abra o arquivo `index.html` diretamente no seu navegador de preferência (Google Chrome, Firefox, etc.).

Não há dependências ou servidores necessários para esta versão MVP.
