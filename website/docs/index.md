---
title: "A new Ginga Developer Ecosystem with ginga.org.br portal, ginga-playground and ginga-code tools"
template: "home.html"
hide:
  - navigation
authors:
  - name: Alan L. V. Guedes
    institution: University of Reading
  - name: Paulo Victor Borges
    institution: PUC-Rio
  - name: Daniel Moraes
    institution: PUC-Rio
  - name: Sergio Colcher
    institution: PUC-Rio
conference: "WTVDI 2026"
links:
  - name: Paper
    url: main.pdf
    icon: ri:file-pdf-2-line
  - name: Slides
    url: slides/
    icon: ri:slideshow-line
  - name: Software Code
    url: https://github.com/alanlivio/gingaf
    icon: ri:github-line
  - name: LaTeX/Website Code
    url: https://github.com/alanlivio/paper-gingaf-ecosystem
    icon: ri:github-line
description: "A new Ginga Developer Ecosystem with ginga.org.br portal, ginga-playground and ginga-code tools."
---

<div class="abstract-container" markdown="1">
<div class="abstract-inner" markdown="1">

## Abstract

Interactive development and debugging of Nested Context Language (NCL) applications remain challenging due to the traditional decoupling between document authoring tools and runtime execution engines. In this paper, we present the new **Ginga Developer Ecosystem**, a unified suite combining the official portal **`ginga.org.br`**, the web-native **`ginga-playground`** (powered by Monaco Editor, debounced compilation, and CanvasKit WebAssembly graphics), and **`ginga-vscode`** (a Visual Studio Code extension providing WebSocket Debug Bridge integration, deterministic Virtual Clock time-stepping, live sourcemapped link highlighting, and reactive property inspection).

</div>
</div>

## Ecosystem Pillars

1. **`ginga.org.br` Official Portal**: Interactive tutorial embedding, deep-linking parameter passing (`?ncl=`, `?code=`), and portal-wide documentation integration.
2. **`ginga-playground` Workbench**: In-browser live authoring environment running `ncl_doc` compiled to WebAssembly with 60 FPS CanvasKit GPU rendering.
3. **`ginga-vscode` Extension**: Full IDE development workflow featuring Webview player tabs, WebSocket Debug Bridge, and sub-millisecond Virtual Clock control.

## Citation

```bibtex
@inproceedings{ginga_ecosystem2026,
  author    = {Guedes, Alan L. V. and Borges, Paulo Victor and Moraes, Daniel and Colcher, Sergio},
  title     = {A new Ginga Developer Ecosystem with ginga.org.br portal, ginga-playground and ginga-code tools},
  booktitle = {Anais Estendidos do XXXII Simpósio Brasileiro de Sistemas Multimídia e Web (WTVDI 2026)},
  location  = {Lavras, Brazil},
  year      = {2026},
  doi       = {10.5753/webmedia.2026.gingaf-ecosystem}
}
```
