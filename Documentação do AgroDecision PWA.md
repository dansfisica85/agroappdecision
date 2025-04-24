# Documentação do AgroDecision PWA

## Visão Geral

O AgroDecision é um Progressive Web App (PWA) para análise climática e tomada de decisões agrícolas. Esta documentação descreve a estrutura, funcionalidades e melhorias implementadas na aplicação.

## Estrutura de Arquivos

```
/
├── index.html              # Arquivo HTML principal
├── manifest.json           # Configurações do PWA
├── sw.js                   # Service Worker para funcionalidades offline
├── css/
│   ├── styles.css          # Estilos principais
│   └── improvements.css    # Estilos adicionais e melhorias
├── js/
│   ├── app.js              # Aplicativo principal e inicialização
│   ├── auth.js             # Autenticação com Firebase
│   ├── charts.js           # Gráficos e visualizações
│   ├── db.js               # Gerenciamento de banco de dados local
│   ├── history.js          # Histórico de simulações
│   ├── home.js             # Tela inicial e recursos de boas-vindas
│   ├── install.js          # Gerenciamento de instalação do PWA
│   ├── map.js              # Funcionalidades do mapa
│   ├── offline.js          # Gerenciamento de recursos offline
│   ├── regional.js         # Consulta regional e notícias
│   └── simulation.js       # Simulação de colheita
├── images/
│   └── logo_AD.png         # Logo do aplicativo
└── icons/
    ├── icon-72x72.png      # Ícones em vários tamanhos para PWA
    ├── icon-96x96.png
    ├── icon-128x128.png
    ├── icon-144x144.png
    ├── icon-152x152.png
    ├── icon-192x192.png
    ├── icon-384x384.png
    └── icon-512x512.png
```

## Funcionalidades Principais

### 1. Mapa Interativo
- Visualização de mapa usando Leaflet.js
- Seleção de localização com marcadores
- Exibição de dados climáticos para a localização selecionada

### 2. Consulta Mensal
- Visualização de dados climáticos mensais
- Gráficos de temperatura e precipitação
- Estatísticas climáticas

### 3. Consulta Regional
- Notícias agrícolas regionais
- Filtragem por região e cultura
- Previsão do tempo regional

### 4. Indicadores
- Índice de seca
- Índice de vegetação
- Risco de geada
- Visualização em gráfico radar

### 5. Simulação de Colheita
- Simulação baseada em parâmetros agrícolas
- Cálculo de produtividade estimada
- Necessidade hídrica
- Ciclo da cultura
- Data estimada de colheita
- Probabilidades de sucesso

### 6. Histórico
- Registro de simulações realizadas
- Visualização detalhada de simulações anteriores
- Organização por data

## Recursos PWA

### 1. Instalação
- Manifest.json configurado para instalação
- Ícones em vários tamanhos
- Prompt de instalação personalizado
- Detecção de instalação

### 2. Funcionamento Offline
- Service Worker com estratégia de cache
- Sincronização de dados quando online
- Indicador de status de conexão
- Armazenamento local de dados

### 3. Atualizações
- Verificação de novas versões
- Notificação de atualização disponível
- Atualização automática do Service Worker

## Melhorias Implementadas

### 1. Estrutura de Código
- Reorganização em módulos JavaScript separados
- Separação de estilos CSS
- Organização em diretórios específicos
- Eliminação de duplicações

### 2. Interface do Usuário
- Tela inicial aprimorada com cards de recursos
- Animações e transições suaves
- Efeitos 3D no logo
- Menu dropdown para usuário
- Tutorial interativo para novos usuários

### 3. Acessibilidade
- Links para pular navegação
- Atributos ARIA para leitores de tela
- Suporte a navegação por teclado
- Melhor contraste e legibilidade
- Textos alternativos para imagens

### 4. Responsividade
- Layout adaptável para dispositivos móveis, tablets e desktops
- Suporte a orientação retrato e paisagem
- Elementos de interface otimizados para toque

### 5. Personalização
- Modo escuro
- Configurações de notificações
- Preferências de sincronização de dados

## Tecnologias Utilizadas

- **HTML5**: Estrutura da aplicação
- **CSS3**: Estilos e animações
- **JavaScript**: Lógica da aplicação
- **IndexedDB**: Armazenamento local de dados
- **Service Worker**: Funcionalidades offline
- **Firebase**: Autenticação e armazenamento em nuvem
- **Leaflet.js**: Mapas interativos
- **Chart.js**: Visualização de dados
- **SweetAlert2**: Diálogos e notificações
- **Three.js**: Efeitos 3D

## Guia de Uso

### Instalação
1. Acesse o aplicativo em um navegador compatível
2. Clique no botão "Instalar" quando solicitado
3. Ou use a opção "Instalar aplicativo" do navegador

### Primeiros Passos
1. Selecione uma localização no mapa
2. Explore as opções do menu lateral
3. Utilize a simulação de colheita para previsões
4. Consulte dados climáticos mensais e regionais

### Configurações
1. Acesse o menu de usuário no canto superior direito
2. Selecione "Configurações"
3. Personalize as opções conforme sua preferência

## Considerações de Segurança

- Configurações sensíveis do Firebase são protegidas
- Autenticação segura com Google
- Dados do usuário são armazenados localmente quando possível
- Conexões seguras via HTTPS

## Limitações Conhecidas

- Algumas funcionalidades requerem conexão à internet (primeira vez)
- Dados climáticos históricos limitados a 30 anos
- Simulações são aproximações baseadas em modelos simplificados

## Desenvolvimento Futuro

- Integração com APIs de satélite para dados em tempo real
- Suporte a mais culturas e parâmetros de simulação
- Notificações push para alertas climáticos
- Compartilhamento de simulações entre usuários
- Exportação de relatórios em PDF
