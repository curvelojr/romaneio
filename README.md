# 📦 Protocolo Digital de Entregas

Aplicação web progressiva (PWA) desenvolvida para a gestão e confirmação de ordens de serviço e entregas em tempo real. O sistema permite que o estafeta consulte as rotas pendentes, visualize detalhes do cliente e anexe comprovativos digitais (fotografia da mercadoria ou assinatura digital no ecrã touch) antes de submeter o protocolo[cite: 1].

---

## 📱 Funcionalidades

* **Autenticação e Identificação:** Ecrã de login com perfil do estafeta e dados do veículo atribuído[cite: 1].
* **Gestão de Ordens de Serviço:**
  * Aba **A Fazer**: Lista de entregas pendentes com dados de cliente, morada, número de pedido e fatura[cite: 1].
  * Aba **Feitas**: Histórico de entregas concluídas com os respetivos comprovativos[cite: 1].
* **Módulo de Comprovativos:**
  * **Captura de Fotografia:** Acesso à câmara com pré-visualização, carimbo de data/hora e botões de validação ou descarte[cite: 1].
  * **Assinatura Digital:** Canvas interativo sensível ao toque/rato para recolha de assinatura com opção de limpeza[cite: 1].
* **Suporte Offline (PWA):** Registo de *Service Worker* e manifesto para instalação como app no smartphone e consulta de dados sem rede.
* **Persistência Local:** Armazenamento automático via `localStorage` para testes imediatos sem necessidade de backend externo.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estrutura semântica e suporte à tag `<canvas>`.
* **CSS3:** Estilização mobile-first, variáveis CSS, layout flexível e design responsivo.
* **JavaScript (Vanilla):** Lógica da aplicação, gestão de estado, manipulação de streams de câmara (`MediaDevices API`) e eventos de toque.
* **PWA:** `manifest.json` para instalação e `sw.js` para cache e funcionamento offline.

---

## 📂 Estrutura do Repositório

```text
romaneio/
├── index.html        # Interface completa, lógica da aplicação e estilos
├── manifest.json     # Metadados e configuração para instalação PWA
├── sw.js             # Service Worker para suporte offline e cache
├── icons/            # Ícones da aplicação para o ecrã inicial
│   ├── icon-192.png
│   └── icon-512.png
└── README.md         # Documentação do projeto