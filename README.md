# XR Showcase - Realidade Aumentada e Virtual

Este repositório contém duas experiências imersivas de Realidade Estendida (XR):

1. **AR Animal Care** - Aplicação de Realidade Aumentada baseada em marcador personalizado (BARCODE e HIRO) para interagir com um gato 3D
2. **VR Gundam Hangar** - Experiência de Realidade Virtual com cenários 360° e navegação por olhar (gaze)

---

## 🐾 Projeto 1: AR Animal Care

### Descrição
Uma experiência de **Realidade Aumentada** onde o utilizador pode interagir com um gato 3D através de marcadores. O sistema reconhece o marcador através da câmara e sobrepõe um gato animado que reage a toques nos itens de comida e água.

### Tecnologias Utilizadas
- **A-Frame** (v1.2.0) - Framework para realidade virtual na web
- **AR.js** (v2.2.2) - Biblioteca para Realidade Aumentada
- **JavaScript puro** - Componentes customizados e lógica de interação
- **HTML5/CSS3** - Interface de utilizador e estilização

### Funcionalidades Implementadas

#### 1. Integração AR.js com A-Frame
- Câmara do dispositivo configurada como fundo da aplicação
- Deteção de marcadores em tempo real (BARCODE e HIRO)
- Renderização de objetos 3D sobre o marcador

#### 2. Marcadores Disponíveis
- **BARCODE** (recomendado) - Mais fácil de detetar
- **HIRO** - Marcador tradicional
- Ambos disponíveis para download diretamente na interface
- Pré-visualização dos marcadores no overlay inicial

#### 3. GUI Overlay (Ecrã Inicial)
- Interface HTML/CSS nativa sobreposta à câmara
- Explicação do conceito do projeto
- Instruções claras de utilização
- Pré-visualização dos marcadores com botões de download
- Botão "Começar" que remove o overlay e inicia a experiência

### Como Utilizar

1. **Aceder à aplicação**: Abrir `AR/index.html` via servidor local (HTTPS ou localhost)
2. **Ler instruções**: O overlay inicial explica o conceito e mostra os marcadores
3. **Baixar o marcador**: Clicar no botão "Baixar PNG" (BARCODE recomendado)
4. **Imprimir ou exibir**: O marcador pode ser impresso ou mostrado noutro dispositivo
5. **Iniciar experiência**: Clicar em "COMEÇAR EXPERIÊNCIA AR"
6. **Permitir câmara**: Autorizar o acesso à câmara quando solicitado
7. **Apontar para o marcador**: Posicionar o marcador à frente da câmara

### Requisitos Técnicos
- Navegador com suporte a WebRTC e WebGL (Chrome, Edge, Safari, Firefox)
- **HTTPS ou localhost** (necessário para acesso à câmara)
- Dispositivo com câmara (PC portátil, tablet ou smartphone)

---

## 🤖 Projeto 2: VR Gundam Hangar

### Descrição
Uma experiência de **Realidade Virtual** imersiva que transporta o utilizador para um hangar futurista. O projeto inclui três cenários panorâmicos 360°, navegação por olhar (gaze) com hotspots interativos, e um modelo 3D detalhado do Gundam RX-78-2.

### Tecnologias Utilizadas
- **A-Frame** (v1.5.0) - Framework para realidade virtual na web
- **WebXR API** - Suporte a headsets de Realidade Virtual
- **JavaScript** - Componentes customizados (Scene Manager)
- **CSS3** - Interface de utilizador sobreposta

### Funcionalidades Implementadas

#### 1. Visor 360° com Múltiplos Cenários
- **3 ambientes panorâmicos diferenciados**:
  - **Hangar Principal**: Base do Gundam RX-78-2
  - **Colónia Espacial Side-7**: Centro de pesquisa da Federação
  - **Campo de Batalha de Jaburo**: Zona de combate intenso
- Texturas de céu 360° (equirectangular) em alta resolução
- Transições suaves entre cenários com efeito de flash

#### 2. Componente Customizado (Scene Manager)
- Componente JavaScript reutilizável `scene-manager`
- Gestão centralizada da troca de texturas do céu (`a-sky`)
- Controlo de visibilidade/escala dos grupos de elementos de cada cenário
- Sistema de eventos para navegação entre cenários
- Efeitos de transição (flash branco) ao teleportar

#### 3. Interação por Olhar (Gaze)
- Câmara com controlos de movimento (`look-controls`)
- Cursor interativo (`a-cursor`) com animações
- **Sistema de fusing**: Utilizador deve olhar para o hotspot durante 1.5 segundos
- Anel de progresso visual durante o fusing
- Hotspots coloridos (azul, vermelho, verde) com textos indicativos
- Pulsação suave dos hotspots para chamar atenção

#### 4. Elementos Espaciais
- **Textos 3D** (`a-text`) em cada cenário para orientação
- Placas informativas e lore contextual
- Elementos decorativos específicos por cenário:
  - Hangar: Grid no chão, anel de energia
  - Colónia: Anéis concêntricos, satélite flutuante
  - Batalha: Chamas, destroços, esferas de energia pulsantes

#### 5. Modelo Gundam 3D
- Construído inteiramente com geometrias primitivas (sem ficheiros externos)
- Componentes detalhados: corpo, cabeça, braços, pernas, omoplatas
- Sabre de luz animado com emissividade
- Olhos LED brilhantes
- Mochila propulsora (boosters)
- Animações suaves de movimento

#### 6. Iluminação e Efeitos Visuais
- Luz direcional principal
- Luzes de preenchimento azul e vermelha
- Pontos de luz dinâmicos com intensidade variável
- Partículas flutuantes de energia

### Como Utilizar

#### Modo Desktop (sem óculos VR)
1. Abrir `VR/index.html` no navegador
2. Arrastar com o rato para rodar a câmara à volta do Gundam
3. Usar a roda do rato para aproximar/afastar
4. Olhar para os hotspots coloridos (círculos) durante 1.5 segundos
5. Aguardar o preenchimento do anel para teleportar entre cenários

#### Modo VR (com óculos)
1. Abrir `VR/index.html` no browser do headset (ex: Meta Quest Browser)
2. Clicar no botão **"🔮 ENTRAR NO MODO VR"**
3. Permitir o acesso à sessão WebXR
4. Explorar o hangar movendo a cabeça
5. Fixar o olhar nos hotspots para navegar entre cenários

### Controles
| Ação | Desktop | Headset VR |
|------|---------|-------------|
| Olhar ao redor | Arrastar mouse | Mover a cabeça |
| Interagir com hotspot | Fixar o cursor no hotspot | Fixar o olhar no hotspot |
| Teleportar | Aguardar 1.5 segundos | Aguardar 1.5 segundos |

### Cenários Disponíveis
| Cenário | Descrição | Hotspots |
|---------|-----------|----------|
| Hangar Principal | Gundam RX-78-2 em manutenção | Portal Azul → Colónia, Portal Vermelho → Batalha |
| Colónia Espacial | Centro de pesquisa Side-7 | Retorno ao Hangar, Avançar para Batalha |
| Campo de Batalha | Zona de combate Jaburo | Retorno ao Hangar, Voltar à Colónia |

---

## 🚀 Como Executar Localmente

### Com Live Server (Recomendado)
1. Instale a extensão **Live Server** no VS Code
2. Abra a pasta do projeto
3. Clique com o botão direito em `index.html` → **Open with Live Server**

### Com Python
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
Aceda a http://localhost:8000

Com Node.js
bash
npx serve
📦 Publicação
Página principal: GitHub Pages

Jogos: itch.io (WebGL builds)

AR: Disponível em ./AR/index.html

VR: Disponível em ./VR/index.html

👤 Autor
PedroBPinheiro
GitHub: PedroBabau
itch.io: PedroBPinheiro

📄 Licença
Projeto desenvolvido para a disciplina de Experiências 3D Interativas.

✅ Notas Finais
A experiência AR utiliza marcadores BARCODE e HIRO com download disponível na interface

A experiência VR suporta WebXR para headsets e mouse drag para desktop

Ambos os projetos utilizam animações por código (tick) e manipulação dinâmica de materiais

A AR requer HTTPS ou localhost para acesso à câmara
