# 🪙 Coinpulse

**Cotações em tempo real e acompanhamento de carteira em um só lugar.**

O Coinpulse é uma aplicação web que permite acompanhar o mercado de criptomoedas e visualizar o desempenho de uma carteira de forma organizada. A plataforma reúne cotações em tempo real, gráficos históricos e registros de compras para apresentar o total investido, o valor atual da carteira e os resultados estimados de lucro ou prejuízo.

Com uma interface responsiva, a aplicação facilita a consulta da evolução dos preços e mantém os registros de compras salvos no navegador para acessos futuros.

O projeto foi desenvolvido durante o curso **Aplicações Front-end em React**, colocando em prática a criação de componentes reutilizáveis, o gerenciamento de estado, a integração com a API e o WebSocket da Binance e a visualização de dados com gráficos interativos.

## Funcionalidades

- **Cotações em tempo real:** acompanhamento dos preços com atualizações recebidas pelo WebSocket da Binance.
- **Visão do mercado:** consulta de criptomoedas, preços e variações em uma lista integrada à interface.
- **Gráficos históricos interativos:** visualização da evolução dos preços nos períodos de 1, 7 e 30 dias, com seleção da criptomoeda.
- **Registro de compras:** inclusão da criptomoeda, da quantidade adquirida e do preço de compra.
- **Histórico de compras:** exibição dos registros, dos mais recentes aos mais antigos, com opção de remoção.
- **Resumo da carteira:** apresentação do total investido, do valor atual e do lucro ou prejuízo estimado.
- **Persistência local:** armazenamento dos registros no navegador por meio do `localStorage`.
- **Indicador de conexão:** exibição do estado da conexão com o serviço de cotações.
- **Interface responsiva:** adaptação do layout para diferentes tamanhos de tela.

## Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
| --- | --- |
| React | Construção da interface com componentes reutilizáveis |
| JavaScript | Implementação da lógica e das interações |
| Vite | Ambiente de desenvolvimento e geração da versão de produção |
| Tailwind CSS | Estilização e adaptação do layout |
| Recharts | Construção dos gráficos históricos interativos |
| Big.js | Cálculos com precisão decimal |
| API REST da Binance | Consulta de cotações e dados históricos |
| WebSocket | Recebimento de atualizações de preços em tempo real |
| localStorage | Armazenamento dos registros de compras no navegador |

## Organização do projeto

```text
Coinpulse-/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── AddPurchaseForm.jsx
│   │   ├── Change.jsx
│   │   ├── ConnectionStatus.jsx
│   │   ├── Header.jsx
│   │   ├── LivePrice.jsx
│   │   ├── Logo.jsx
│   │   ├── MarketList.jsx
│   │   ├── PortfolioSummary.jsx
│   │   ├── PriceChart.jsx
│   │   └── PurchaseTable.jsx
│   ├── data/
│   │   └── coins.js
│   ├── hooks/
│   │   ├── useCandles.js
│   │   ├── useLivePrices.js
│   │   └── useLocalStorage.js
│   ├── lib/
│   │   ├── binance.js
│   │   ├── format.js
│   │   ├── money.js
│   │   └── purchases.js
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .gitignore
├── .oxlintrc.json
├── index.html
├── package-lock.json
├── package.json
├── README.md
└── vite.config.js
```

### Responsabilidade dos arquivos

| Caminho | Responsabilidade |
| --- | --- |
| `public/` | Armazenamento de arquivos estáticos |
| `src/components/` | Componentes visuais, como formulário, tabela de compras, cotações e gráfico |
| `src/data/` | Informações das criptomoedas disponíveis |
| `src/hooks/` | Hooks personalizados para cotações, histórico de preços e armazenamento local |
| `src/lib/` | Integração com a Binance, cálculos e funções auxiliares |
| `src/App.jsx` | Integração dos componentes e gerenciamento dos principais estados |
| `src/index.css` | Estilos e configurações visuais da aplicação |
| `src/main.jsx` | Inicialização da aplicação React |

## Aprendizados aplicados

O desenvolvimento do Coinpulse permitiu aplicar conceitos de desenvolvimento front-end em uma aplicação integrada a dados de mercado:

- **Componentização:** divisão da interface em componentes com responsabilidades definidas.
- **Comunicação por props:** compartilhamento de dados e ações entre componentes.
- **Gerenciamento de estado:** uso de `useState` para controlar seleções e interações.
- **Gerenciamento de efeitos:** uso de `useEffect` para consultas e conexões com serviços externos.
- **Hooks personalizados:** organização e reutilização da lógica de acesso a dados e persistência.
- **Integração com serviços externos:** consumo de API REST e recebimento de dados via WebSocket.
- **Persistência no navegador:** manutenção dos registros entre acessos com `localStorage`.
- **Visualização de dados:** apresentação do histórico de preços em gráficos interativos.
- **Precisão decimal:** utilização de Big.js nos cálculos da carteira.
- **Responsividade:** construção de um layout adaptável com Tailwind CSS.

## Sobre os dados

Os registros de compras permitem acompanhar e simular o desempenho de uma carteira. A aplicação não executa operações financeiras nem movimenta criptomoedas.

As compras são armazenadas localmente no navegador utilizado, sem sincronização entre dispositivos. A limpeza dos dados do navegador pode remover esses registros.

As cotações e os gráficos dependem de conexão com a internet e da disponibilidade dos serviços da Binance.

