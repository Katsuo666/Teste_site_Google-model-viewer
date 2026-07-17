========================================================================
      PROJETO TESTE: Google <model-viewer> (3D + AR Nativa)
========================================================================

1. DESCRIÇÃO GERAL
------------------
Este projeto demonstra a utilização do componente Web oficial da Google 
(<model-viewer>) para renderização 3D interativa de produtos com transição 
direta para Realidade Aumentada Nativa no sistema operativo móvel (Scene Viewer 
em Android e AR Quick Look em iOS).

2. ESTRUTURA DE FICHEIROS
-------------------------
/ (Raiz do Projeto)
│
├── index.html               # Ficheiro HTML com o elemento <model-viewer>
├── README.txt               # Documentação técnica do projeto
└── assets/
    ├── 02_Bolsos.glb        # Modelo 3D principal (Android / Web)
    └── 02_Bolsos.usdz       # (Opcional) Ficheiro otimizado para iOS Quick Look

3. TECNOLOGIAS E DEPENDÊNCIAS
-----------------------------
- HTML5 / CSS3 / JavaScript
- Google <model-viewer> (Web Component importado via CDN unpkg/skypack)
- AR Nativa: WebXR Device API, Android Scene Viewer, Apple AR Quick Look

4. FUNCIONALIDADES E ATRIBUTOS PRINCIPAIS
-----------------------------------------
- 'ar': Ativa a funcionalidade e o botão de Realidade Aumentada.
- 'ar-modes="webxr scene-viewer quick-look"': Define a ordem de prioridade dos motores 
  de AR para máxima compatibilidade entre Android e iOS.
- 'camera-controls': Permite ao utilizador rodar (360°), inclinar e fazer zoom no 
  modelo 3D através de gestos no ecrã antes de entrar na câmara.
- 'shadow-intensity="1"': Adiciona sombras em tempo real para aumentar o realismo 
  na projeção de superfície.
- 'auto-rotate': (Opcional) Ativa a rotação automática do modelo no visualizador.

5. COMO EXECUTAR
----------------
1. Colocar os ficheiros num servidor Web com suporte a HTTPS (obrigatório para AR).
2. Abrir o ficheiro 'index.html' no browser de qualquer dispositivo móvel ou de trabalho.

6. COMO TESTAR
--------------
1. Ao abrir o site, o modelo 3D pode ser inspecionado interativamente em ecrã plano.
2. Clica no botão "Ver no seu espaço" (ou no ícone de AR no canto inferior direito).
3. Aponta a câmara do telemóvel para uma superfície plana (mesa ou chão).
4. O bolso será projetado em tamanho real na superfície, permitindo andar à volta dele no espaço físico.