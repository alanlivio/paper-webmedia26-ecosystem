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
</style>

<!--
_paginate: false
_header: ""
-->

<div style="display: grid; grid-template-columns: 3fr 1fr; align-items: center;">

<div>

# A New Ginga Developer Ecosystem: ginga.org.br Portal, ginga-playground and ginga-code Tools

**Alan L. V. Guedes**$^1$, **Paulo Victor Borges**$^2$, **Daniel Moraes**$^2$, **Sergio Colcher**$^2$
$^1$University of Reading, UK | $^2$PUC-Rio, Brazil

*XXXII Simpósio Brasileiro de Sistemas Multimídia e Web (WebMedia 2026)*

**Paper Website (slides, code, demo)**:
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

- **Context**
- **Proposed Solution**
- **Results**
- **Final Remarks**

---

# Motivation & Context

**Widespread DTV Deployment**
- Ginga (ITU-T H.761 / ABNT 15606-2) is installed on 100% of certified Digital TV receivers in Latin America.
- Reaches over 60 million people daily.

**The Developer Challenge**
- Authoring and execution have been constrained by the lack of lightweight developer tooling.
- Traditional development required native Linux toolchains, manual C++ compilation, or hardware set-top boxes.

**Goal**
- Lower barriers to entry for Ginga development with zero-install, modern web and IDE tools.

---

# The Three Pillars of the Ecosystem

**Pillar 1: `ginga.org.br` Web Portal**
- Centralized knowledge hub, NCL handbook, tutorials, and standard references.

**Pillar 2: `ginga-playground` Workbench**
- Browser-native interactive environment to edit and run NCL and HTML5 applications instantly.

**Pillar 3: `ginga-code` VS Code Extension**
- IDE integration offering syntax highlighting, application launching, and live debug bridge.

---

# Pillar 1: ginga.org.br Web Portal

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Modern Architecture**
- Built with modern static site generation (Zensical).
- Multilingual documentation: Portuguese, Spanish, and English.

**Hosted Resources**
- Getting started guides for new Ginga developers.
- Comprehensive NCL tag and attribute handbook.
- Official SBTVD and ITU-T specifications.
- Curated examples and interactive code snippets.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/portal2.png" />

</div>

</div>

---

# Pillar 2: ginga-playground Workbench

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Zero-Installation Web Execution**
- Runs directly inside any modern browser using WebAssembly / CanvasKit.
- Powered by the headless `gingaf` engine.

**Interactive Capabilities**
- Split-pane layout: code editor on the left, live TV preview on the right.
- Pre-loaded interactive catalog of NCL, Lua, and HTML5 sample applications.
- Instant re-rendering upon code edits without page reload.
- Virtual remote control interface to simulate DTV keypresses.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/playground.png" />

</div>

</div>

---

# Pillar 3: ginga-code VS Code Extension

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Official Marketplace Availability**
- Published directly to Visual Studio Code Marketplace and Open VSX.

**Modern Developer Workflows**
- Rich XML and NCL syntax awareness and schema validation.
- One-click launch to preview applications locally or in the browser.
- Debug bridge connecting IDE breakpoints to `gingaf` execution states.
- Template generation for rapid prototyping of TV 2.5 and TV 3.0 applications.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/vscode.png" />

</div>

</div>

---

# Ecosystem Architecture

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

**Unified Backbone**
- All three pillars converge on the decoupled `gingaf` engine architecture.
- Shared parser and execution semantics across web and desktop workflows.

**Workflow Synergy**
- Developers learn concepts on `ginga.org.br`.
- Prototype and share minimal reproducible examples via `ginga-playground`.
- Build production applications in Visual Studio Code with `ginga-code`.

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/ecosystem.png" />

</div>

</div>

---

# Final Remarks

- Successfully eliminates high setup friction for digital television interactive application development.
- Provides zero-install accessibility for students, researchers, and professional broadcast developers.
- Entire ecosystem is open-source and publicly hosted under the `ginga-org-br` organization.
- Accessible online at `http://ginga.org.br`.

---

<!--
_paginate: false
_header: ""
-->

# Thank You!

<div style="display: grid; grid-template-columns: 3fr 2fr; align-items: start;">

<div>

### Questions & Discussion

- **Portal**: https://ginga.org.br
- **Playground**: https://ginga.org.br/gingaf/playground/
- **VS Code Extension**: https://marketplace.visualstudio.com/items?itemName=ginga-org-br.ginga-code
- **Repository**: https://github.com/ginga-org-br
- **Contact**: `a.guedes@reading.ac.uk` | `danielmoraes@telemidia.puc-rio.br`

</div>

<div style="display: flex; justify-content: center; align-items: flex-start;">

<img src="assets/portal1.png" />

</div>

</div>
