---
marp: true
theme: default
paginate: true
header: 'Ginga Developer Ecosystem — WTVDI / WebMedia 2026'
---

<style>
.grayscale {
  filter: grayscale(100%);
}
.grid-2x2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 14px 28px;
  width: 100%;
  margin-top: 8px;
}
.grid-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 18px;
  width: 100%;
  margin-top: 18px;
}
.grid-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.grid-card img {
  width: 100%;
  max-height: 165px;
  object-fit: contain;
  border-radius: 6px;
  border: 1px solid transparent;
  background-color: transparent;
  box-shadow: none;
}
.grid-card p {
  margin: 6px 0 0 0;
  font-size: 18px;
  font-weight: 600;
  line-height: 1.3;
  color: #1f2328;
}
.grid-card a {
  color: #0969da;
  font-weight: 700;
  text-decoration: underline;
}
</style>

<!--
_paginate: false
_header: ""
-->

<div style="display: grid; grid-template-columns: 3fr 1fr; align-items: center;">

<div>

# A New Ginga Developer Ecosystem: ginga.org.br Portal, ginga-playground and ginga-code Tools

**Alan L. V. Guedes**$^1$, **Paulo Victor Borges**$^2$, **Daniel Moraes**$^2$, **Sergio Colcher**$^2$
$^1$University of Reading, UK | $^2$PUC-Rio, BR

*XXXII Simpósio Brasileiro de Sistemas Multimídia e Web (WebMedia 2026)*

**Website do Artigo (slides, código, demo)**:
https://alanlivio.github.io/paper-webmedia26-ecosystem/

</div>

<div style="display: flex; flex-direction: column; justify-content: center;">

<img src="assets/uor.svg" height="200" class="grayscale" />
<img src="assets/puc-rio.svg" height="120" class="grayscale" />
<img src="assets/qrcode.svg" height="250" />

</div>

</div>

---

# Agenda

- **Contexto e Definição do Problema**
- **Solução Proposta**
- **Considerações Finais**

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Contexto e Definição do Problema

---

# O Middleware de DTV Ginga

<div style="display: flex; flex-direction: column; gap: 14px; margin-top: 10px; width: 100%;">
  <div style="display: flex; justify-content: space-between; gap: 24px; width: 100%;">
    <div style="flex: 1 1 0; min-width: 0; display: flex; justify-content: center; align-items: center; height: 215px;">
      <img src="assets/Picture1.png" style="max-height: 215px; max-width: 100%; object-fit: contain; border-radius: 6px; border: 1px solid #d0d7de; box-shadow: 0 4px 12px rgba(0,0,0,0.12);" />
    </div>
    <div style="flex: 1 1 0; min-width: 0; display: flex; justify-content: center; align-items: center; height: 215px;">
      <img src="assets/Picture2.jpg" style="max-height: 215px; max-width: 100%; object-fit: contain; border-radius: 6px; border: 1px solid #d0d7de; box-shadow: 0 4px 12px rgba(0,0,0,0.12);" />
    </div>
  </div>
  <div style="display: flex; justify-content: space-between; gap: 24px; width: 100%;">
    <div style="flex: 1 1 0; min-width: 0; display: flex; justify-content: center; align-items: center; height: 215px;">
      <img src="assets/Picture3.png" style="max-height: 215px; max-width: 100%; object-fit: contain; border-radius: 6px; border: 1px solid #d0d7de; box-shadow: 0 4px 12px rgba(0,0,0,0.12);" />
    </div>
    <div style="flex: 1 1 0; min-width: 0; display: flex; justify-content: center; align-items: center; height: 215px;">
      <img src="assets/Picture4.jpg" style="max-height: 215px; max-width: 100%; object-fit: contain; border-radius: 6px; border: 1px solid #d0d7de; box-shadow: 0 4px 12px rgba(0,0,0,0.12);" />
    </div>
  </div>
</div>

Definido na série de normas SBTVD ABNT 15606.

Presente em receptores de TV Digital certificados no Brasil e América Latina (>60M telespectadores)

---

# Ecossistema de Desenvolvimento Ginga é limitado

**Ausência de ambiente portátil e "zero-install"**: de fácil acesso, completo e aberto.
- Podemos comparar o Mozilla https://developer.mozilla.org/ e a Ginga-VM (2010)

<div style="display: flex; justify-content: center; gap: 24px; align-items: center; margin-top: 12px;">
  <img src="assets/image.png" style="width: 500px; object-fit: contain;" />
  <img src="assets/image-1.png" style="width: 500px; object-fit: contain;" />
</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Solução Proposta

---

# Os Quatro Pilares do Ecossistema

**Pilar 1: Motor de Execução `gingaf`**
- Ambiente desacoplado e multiplataforma para execução de aplicações NCL e HTML5.

**Pilar 2: Portal Web `ginga.org.br`**
- Centro unificado de conhecimento, manual do NCL, tutoriais e referências aos padrões técnicos.

**Pilar 3: Ambiente Interativo `ginga-playground`**
- Ambiente web interativo para editar e executar aplicações NCL e HTML5 instantaneamente no navegador.

**Pilar 4: Extensão para VS Code `ginga-code`**
- Integração com IDE oferecendo destaque de sintaxe, execução de aplicações e ponte de depuração em tempo real.

---

# Arquitetura do Ecossistema

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Núcleo Unificado**
- Todos os quatro pilares convergem na arquitetura desacoplada do motor `gingaf`.
- Semântica compartilhada de análise sintática e execução em fluxos de trabalho desktop e web.

**Sinergia de Fluxo de Trabalho**
- Desenvolvedores aprendem conceitos em `ginga.org.br`.
- Prototipam e compartilham exemplos mínimos reproduzíveis através do `ginga-playground`.
- Constroem aplicações prontas para produção no Visual Studio Code com o `ginga-code`.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/ecosystem.png" />

</div>

</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Pilar 1: gingaf

---

# Pilar 1: gingaf

## NCL com Links, Grade de Vídeos, NCL Embutido e Navegação

<div class="grid-2x2">
  <div class="grid-card">
    <img src="assets/gifs/video.ncl.gif" alt="video.ncl" />
    <p>NCL com links básicos (<a href="https://ginga.org.br/gingaf/playground/?app=video.ncl">video.ncl</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/video_grid.ncl.gif" alt="video_grid.ncl" />
    <p>NCL com grade de vídeos (<a href="https://ginga.org.br/gingaf/playground/?app=video_grid.ncl">video_grid.ncl</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/emb_ncl.ncl.gif" alt="emb_ncl.ncl" />
    <p>NCL embutido em NCL (<a href="https://ginga.org.br/gingaf/playground/?app=emb_ncl.ncl">emb_ncl.ncl</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/focus_nav.ncl.gif" alt="focus_nav.ncl" />
    <p>NCL com navegação de foco e seleção (<a href="https://ginga.org.br/gingaf/playground/?app=focus_nav.ncl">focus_nav.ncl</a>)</p>
  </div>
</div>

---

# Pilar 1: gingaf

## NCLua, HTML+CCWS, HTML Embutido e Multiusuário

<div class="grid-2x2">
  <div class="grid-card">
    <img src="assets/gifs/lua_canvas.ncl.gif" alt="lua_canvas.ncl" />
    <p>NCL com desenho em tela Lua e teclas (<a href="https://ginga.org.br/gingaf/playground/?app=lua_canvas.ncl">lua_canvas.ncl</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/current_service.html.gif" alt="current_service.html" />
    <p>HTML com CCWS /current-service/ (<a href="https://ginga.org.br/gingaf/playground/?app=current_service.html">current_service.html</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/emb_html.ncl.gif" alt="emb_html.ncl" />
    <p>NCL com documento HTML embutido (<a href="https://ginga.org.br/gingaf/playground/?app=emb_html.ncl">emb_html.ncl</a>)</p>
  </div>
  <div class="grid-card">
    <img src="assets/gifs/multiuser_profile.gif" alt="multiuser_profile/main.ncl" />
    <p>NCL com troca de perfil multiusuário e publicidade direcionada (<a href="https://ginga.org.br/gingaf/playground/?app=multiuser_profile/main.ncl">multiuser_profile/main.ncl</a>)</p>
  </div>
</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Pilar 2: Portal Web ginga.org.br

---

# Pilar 2: Portal Web ginga.org.br

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Arquitetura Moderna**
- Construído com gerador de sites estáticos moderno (Zensical).
- Documentação multilíngue: português, espanhol e inglês.

**Recursos Hospedados**
- Guias introdutórios para novos desenvolvedores Ginga.
- Manual abrangente de tags e atributos do NCL.
- Especificações oficiais do SBTVD e da ITU-T.
- Exemplos selecionados e trechos interativos de código.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/portal2.png" />

</div>

</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Pilar 3: Ambiente Interativo ginga-playground

---

# Pilar 3: Ambiente Interativo ginga-playground

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Execução Web Sem Instalação**
- Executa diretamente em qualquer navegador moderno usando WebAssembly / CanvasKit.
- Impulsionado pelo motor desacoplado `gingaf`.

**Capacidades Interativas**
- Layout dividido: editor de código à esquerda, pré-visualização ao vivo da TV à direita.
- Catálogo interativo pré-carregado com aplicações de exemplo em NCL, Lua e HTML5.
- Renderização instantânea após edições de código, sem recarregar a página.
- Controle remoto virtual para simular o pressionamento de teclas da DTV.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/playground.png" />

</div>

</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Pilar 4: Extensão para VS Code ginga-code

---

# Pilar 4: Extensão para VS Code ginga-code

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Disponibilidade Oficial no Marketplace**
- Publicada diretamente no Visual Studio Code Marketplace e Open VSX.

**Fluxos de Trabalho Modernos**
- Reconhecimento de sintaxe e validação de esquemas XML e NCL.
- Execução com um clique para pré-visualizar aplicações localmente ou no navegador.
- Ponte de depuração conectando breakpoints da IDE aos estados de execução do `gingaf`.
- Geração de templates para prototipagem rápida de aplicações de TV 2.5 e TV 3.0.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/vscode.png" />

</div>

</div>

---

<!-- _class: invert -->
<!-- _paginate: skip -->

# Considerações Finais

---

# Considerações Finais

**Contribuições Principais**:
- **Portal `ginga.org.br`**: Hub unificado de documentação e especificações para a comunidade Ginga.
- **`ginga-playground`**: Workbench web interativo no navegador para prototipação sem instalação local.
- **`ginga-code`**: Extensão para VS Code que integra launcher e execução direta no desktop.

**Impacto**: Elimina o atrito inicial de configuração e viabiliza acesso imediato a estudantes, pesquisadores e desenvolvedores (código aberto em `https://ginga.org.br`).

---

<!--
_paginate: false
_header: ""
-->

# Obrigado!

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

### Dúvidas e Discussão

- **Portal**: https://ginga.org.br
- **Playground**: https://ginga.org.br/gingaf/playground/
- **Extensão VS Code**: https://marketplace.visualstudio.com/items?itemName=ginga-org-br.ginga-code
- **Repositório**: https://github.com/ginga-org-br
- **Contato**: `a.guedes@reading.ac.uk` | `danielmoraes@telemidia.puc-rio.br`

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/portal1.png" />

</div>

</div>
