# MVP NeoBank+

[cite_start]Este é o repositório do MVP (Minimum Viable Product) para o projeto NeoBank+, um banco digital inteligente[cite: 299]. [cite_start]Este projeto foi desenvolvido como parte da atividade acadêmica "Ciclo Completo de Desenvolvimento de Software" (Tema 6)[cite: 295, 296].

[cite_start]O foco deste MVP é demonstrar a interface do usuário (UI) e as interações *mockadas* (simuladas) das principais funcionalidades, conforme especificado nos requisitos de implementação.

## 🚀 Funcionalidades do MVP Implementadas

Este protótipo é uma SPA (Single Page Application) estática que simula o fluxo de um banco digital. As seguintes funcionalidades estão presentes:

1.  [cite_start]**Cadastro de Conta Digital Simples** 
    * **Onde:** Página "Abrir Conta".
    * **O que faz:** Um formulário de cadastro que, ao ser enviado, exibe uma mensagem de sucesso simulada e redireciona o usuário para o Dashboard.

2.  [cite_start]**Transferência PIX Mockada** 
    * **Onde:** Página "PIX".
    * **O que faz:** Permite o preenchimento de uma chave e valor. Ao enviar, exibe uma mensagem de sucesso simulada.

3.  [cite_start]**Emissão de Cartão Virtual Mockado** [cite: 340]
    * **Onde:** Página "Cartões".
    * **O que faz:** Ao clicar no botão "Emitir Cartão Virtual", um cartão virtual simulado é exibido na tela.

4.  [cite_start]**Dashboard com Saldo e Extrato** [cite: 341]
    * **Onde:** Página "Dashboard".
    * **O que faz:** Exibe um saldo estático e uma lista de transações recentes (extrato) com dados fixos.

5.  [cite_start]**Alerta de Transação Suspeita (Simulação)** [cite: 342]
    * **Onde:** Página "Dashboard".
    * [cite_start]**O que faz:** Um alerta de segurança estático é exibido no topo do dashboard para simular a detecção de fraude[cite: 49].

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estrutura semântica do site.
* **CSS3:** Estilização completa, incluindo:
    * Design Responsivo (Mobile-first).
    * Modo Escuro (Dark Mode) com `body.dark-mode`.
    * Variáveis CSS para gerenciamento de tema.
* **JavaScript (ES6+):**
    * Manipulação do DOM.
    * Simulação de SPA (Single Page Application) para navegação sem recarregar a página.
    * Persistência do tema (Modo Escuro) usando `localStorage`.
    * Simulação de eventos de formulário (submit).

## [cite_start]⚙️ Setup e Instalação (README com setup) 

Como este projeto é um MVP estático (frontend puro) sem a necessidade de um backend ou compilação, o setup é muito simples:

1.  **Clonar o repositório:**
    ```bash
    git clone https://[URL-DO-SEU-REPOSITORIO]/neobank-mvp.git
    ```

2.  **Abrir o projeto:**
    * Navegue até a pasta do projeto (`cd neobank-mvp`).
    * Abra o arquivo `index.html` diretamente no seu navegador de preferência (Google Chrome, Firefox, etc.).

Não há dependências ou servidores necessários para esta versão MVP.

---
