# XR Showcase - Realidade Aumentada e Virtual

Este repositório contém duas experiências imersivas de Realidade Estendida (XR): uma aplicação de **Realidade Aumentada (AR)** focada no cuidado de animais, e uma experiência de **Realidade Virtual (VR)** ambientada num hangar mecanizado.

---

## 📁 Estrutura do Projeto

projeto/
├── index.html # Página inicial para navegar entre os projetos
├── README.md # Este arquivo
├── AR/
│ └── index.html # Projeto AR Animal Care
└── VR/
└── index.html # Projeto VR Robô Hangar


---

## 🐾 Projeto 1: AR Animal Care (Realidade Aumentada)

### Descrição
Uma experiência de Realidade Aumentada onde o utilizador pode alimentar e dar água a animais virtuais através da câmara do dispositivo. Os elementos 3D (comida, água) surgem sobre o mundo real e reagem ao toque, proporcionando feedback visual e sonoro.

### Tecnologias Utilizadas
- **Three.js** - Renderização 3D e gestão da cena
- **WebRTC (getUserMedia)** - Acesso à câmara ao vivo
- **Raycaster** - Deteção de toque/clique nos objetos 3D
- **Web Audio API** - Efeitos sonoros de interação

### Funcionalidades
- 📷 **Câmara ao vivo** como fundo da experiência AR
- 🍎 **Dois modos de interação**:
  - **Modo Comida**: Maçãs, cenouras e tigelas de ração
  - **Modo Água**: Gotas, tigelas de água e garrafas
- 🐕 **Animais 3D interativos** (cães, gatos, coelhos) que saltam ao serem alimentados
- ✨ **Efeitos visuais** (partículas, brilho) e sonoros no momento da interação
- 🖱️ **Compatível com toque (mobile) e clique (PC)**

### Como Utilizar
1. Abrir o ficheiro `AR/index.html` num servidor local ou via HTTPS
2. Permitir o acesso à câmara quando solicitado
3. Escolher entre o modo **Comida** ou **Água** clicando no botão correspondente
4. Apontar a câmara para uma superfície plana
5. Tocar/clicar nos itens flutuantes (cenoura, maçã, gota, etc.)
6. Observar os animais a saltar e a reagir com feedback sonoro

### Requisitos
- Navegador com suporte a `getUserMedia` (Chrome, Edge, Safari, Firefox)
- **HTTPS ou localhost** (para acesso à câmara)
- Dispositivo com câmara (PC ou mobile)

> ⚠️ **Nota**: Em alguns navegadores mobile, é necessário tocar primeiro no ecrã para ativar o áudio.

---

## 🤖 Projeto 2: VR Gundam Hangar (Realidade Virtual)

### Descrição
Uma experiência de Realidade Virtual imersiva que transporta o utilizador para um hangar futurista, onde pode observar e interagir com um robô estilizado. O ambiente conta com iluminação dinâmica, partículas de energia e efeitos de pós-processamento (glow).

### Tecnologias Utilizadas
- **Three.js** - Motor gráfico 3D
- **WebXR API** - Suporte a headsets de Realidade Virtual
- **EffectComposer + UnrealBloomPass** - Efeitos de glow e brilho
- **OrbitControls** - Navegação desktop/mobile por arrasto

### Funcionalidades
- 🥽 **Suporte WebXR completo** - Compatível com Meta Quest, HTC Vive, etc.
- 🖱️ **Controle desktop** - Arrastar com o rato para olhar à volta (OrbitControls)
- 🤖 **Modelo Robô detalhado** construído com geometrias primitivas:
  - Torso, cabeça com olhos LED, braços, pernas, omoplatas
  - Sabre de luz animado
  - Mochila de propulsão (boosters)
- ✨ **Efeitos ambientais**:
  - Partículas flutuantes de energia
  - Luzes dinâmicas com intensidade variável
  - Grid tecnológico no chão
  - Pilares de hangar e naves decorativas
- 🔘 **Botão dedicado** para entrar em modo VR (headsets)

### Como Utilizar
#### No computador (sem óculos VR):
1. Abrir `VR/index.html`
2. Arrastar com o rato para rodar a câmara à volta do Robô
3. Usar a roda do rato para aproximar/afastar

#### Com óculos de Realidade Virtual (ex: Meta Quest):
1. Abrir `VR/index.html` no browser do headset
2. Clicar no botão **"🔮 ENTRAR NO MODO VR"**
3. Permitir o acesso à sessão WebXR
4. Explorar o hangar em 360° movendo a cabeça

### Requisitos
- Navegador com suporte a WebGL e WebXR:
  - **Desktop**: Chrome, Edge, Firefox (modo VR opcional)
  - **Mobile/VR**: Meta Quest Browser, Firefox Reality, Chrome com WebXR ativado
- Recomendado: hardware com capacidade gráfica para efeitos de bloom

---