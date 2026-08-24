<h1 align="center">Jorge David Diaz Cordero</h1>

<p align="center">
  <strong>Full Stack Developer — frontend-heavy, architecture-obsessed, AI-native.</strong><br>
  I build design systems that survive contact with a real team, and side projects
  that force me to write the hard part myself.
</p>

<p align="center">
  <a href="https://jorgedaviddiaz.com"><img src="https://img.shields.io/badge/Portfolio-jorgedaviddiaz.com-111111?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/jorge-david-diaz-cordero-web-developer/?locale=en_US"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Bogotá,%20Colombia-remote-2E7D32?style=for-the-badge" alt="Location">
</p>

---

## The short version

I started in 2022 doing what everyone does: shipping features and hoping the codebase
would sort itself out. It didn't.

The turning point was inheriting an internal platform written in **vanilla JavaScript** —
no framework, no build step, no bundler. Just the DOM and me. That project taught me more
than any tutorial ever did, because there was nothing to hide behind. No `useState` to
paper over a bad data model. No framework convention to blame. If the state was wrong,
*I* had modeled it wrong.

That's the lens I bring to everything now: **concepts before code**. Understand the
problem, model it honestly, then pick the tool.

Today I work as a Full Stack Developer at **IXCOMERCIO** (remote, since Oct 2023), where I:

- Designed and built a **Storybook component library from scratch** (Atomic Design +
  React composition patterns), cutting new-feature scaffolding from ~2 weeks to 3–4 days.
- Established a **feature-based frontend architecture** using the Proximity Principle,
  and wrote the internal wiki that keeps the team aligned on it.
- Wired **MCP (Model Context Protocol)** between Figma and Claude Code / Cursor so
  design-to-component stopped being a manual translation job.
- Trained ~5 developers on modern React patterns and AI-assisted workflows.

Before that: **NestJS + GraphQL** backends at SERVIAP GROUP, and the **design tokens +
real-time WebSocket ticker** for a crypto exchange at Bitrus.

**On AI:** I don't think the model is the interesting part. The interesting part is that
you have to *know what to ask*, and know when the answer is wrong. We direct — AI executes.
Every project below was built with that assumption.

---

## What I've been building

### 🎮 PixelForge — browser-based 2D game builder

<a href="https://pixelforge-teal.vercel.app">
  <img src="https://raw.githubusercontent.com/JDavidcor23/pixelforge/master/src/assets/presentation.png" alt="PixelForge — sprite editor with layers, timeline and AI panel" width="100%">
</a>

Draw pixel art, animate it frame by frame, build the scene, publish the game. The whole
loop, in the browser.

The hard part wasn't the UI — it was the **infinite canvas**: a Konva.js surface that tracks
its container with `ResizeObserver` and draws from centered offsets instead of CSS centering,
so zoom stays stable at any layer count while holding 60 FPS. State lives in **modular Zustand
slices** (pixels, tools, layers, history) with strictly granular selectors, because one
fat store re-rendering the canvas on every brush stroke is how you lose those 60 FPS.

`Next.js 14` · `TypeScript` · `Konva.js` · `Phaser` · `Zustand` · `Tailwind` · `Supabase`

**[→ Live demo](https://pixelforge-teal.vercel.app)** · **[→ Repo](https://github.com/JDavidcor23/pixelforge)**

---

### 🧙 Albus — the agent that runs your agents

<p align="center">
  <img src="https://raw.githubusercontent.com/JDavidcor23/albus_agent/main/docs/logo.png" alt="Albus" width="140">
</p>

<img src="https://raw.githubusercontent.com/JDavidcor23/albus_agent/main/docs/architecture.png" alt="Albus architecture — one agent that reads your rules and dispatches to capabilities" width="100%">

Automation today asks you to think like a plumber. A Zap here, a script there, a cron job
on a Raspberry Pi you forgot the password to. Six months later you have **forty automations
and no system** — each knows a sliver of context, none of them know *you*.

Albus is a desktop container where those live as agents you can talk to. The design bet
that makes it different: **an agent is a Markdown file in your folder, not code.** You don't
configure a `noNightShifts` flag — you write "nothing with Java, and no night shifts" in
plain English and the agent reads the whole file. Its memory is a text file you can open,
correct, and delete. A memory only the program understands is a memory you can't audit the
day it does something strange.

`Electron` · `React` · `TypeScript` · `Supabase` · `WebSockets` · `Zod` · `Tesseract.js` · `Cytoscape`

**[→ Repo](https://github.com/JDavidcor23/albus_agent)**

---

### ☁️ Cloud Quest — learn AWS by fighting it, not reading about it

<p align="center">
  <img src="https://raw.githubusercontent.com/JDavidcor23/aws_island/main/docs/screens/01-menu.png" width="49%" alt="Main menu">
  <img src="https://raw.githubusercontent.com/JDavidcor23/aws_island/main/docs/screens/06-elegir-carta.png" width="49%" alt="Choosing a card against the boss">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/JDavidcor23/aws_island/main/docs/screens/09-remate.png" width="49%" alt="Finisher — the cloud answers">
  <img src="https://raw.githubusercontent.com/JDavidcor23/aws_island/main/docs/screens/10-victoria.png" width="49%" alt="The island comes back to life">
</p>

A turn-based RPG built for the **AWS Hackathon 2026**. A rookie lands on an island that's
shutting down — the whole town ran on one old machine, and it can't take it anymore.
You beat the **Legacy Server** by answering every problem it screams with the cloud
characteristic that solves it.

The design rule the whole thing is built on: **learning is a CONSEQUENCE of fun, never the
price of admission.** The boss never says "this is Rapid Elasticity" — it screams
*"100,000 users just showed up at once!"* You discover the concept by surviving it.
Four of the five NIST essential characteristics, and not one paragraph of theory before
the punch lands.

`React` · `Canvas 2D` · `Zustand` · `Vite` · `Vitest`

**[→ Live demo](https://aws-island.vercel.app)** · **[→ Repo](https://github.com/JDavidcor23/aws_island)**

---

### 🎸 Rock Hero — a rhythm game with no rhythm-game library

<a href="https://guitar-hero-react.vercel.app">
  <img src="https://res.cloudinary.com/dhu6ga6hl/image/upload/v1773102994/guitarhero/z0rwbigbgrvnphkguhws.png" alt="Rock Hero — note highway rendered on Canvas 2D" width="100%">
</a>

Guitar Hero in the browser. The interesting constraint: **`requestAnimationFrame` is not a
clock.** Drive a rhythm game off frame time and it drifts out of sync within seconds, so the
engine runs entirely on `AudioContext.currentTime` — the audio hardware is the source of
truth, the render loop just draws whatever the clock says should be on screen.

Everything else is written from scratch too: the **`.chart` parser** (Clone Hero format,
no external library), the Canvas 2D perspective math for the note highway, **multi-channel
stems** that mute the instrument you're failing, and real-time audio/video offset calibration.
Organized by the **Proximity Principle** — features are self-contained, not scattered across
`components/`, `hooks/`, `utils/`.

`React 19` · `TypeScript` · `Vite` · `Web Audio API` · `Canvas 2D` · `Gamepad API`

**[→ Live demo](https://guitar-hero-react.vercel.app)** · **[→ Repo](https://github.com/JDavidcor23/Guitar-Hero-React)**

---

## Stack

Things I actually reach for — not everything I've ever opened.

**Core**

![JavaScript](https://img.shields.io/badge/JavaScript_ES6+-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232a?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![CSS](https://img.shields.io/badge/Modern_CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**State & data**

![Zustand](https://img.shields.io/badge/Zustand-443E38?style=for-the-badge)
![TanStack Query](https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=react-query&logoColor=white)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-593d88?style=for-the-badge&logo=redux&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)

**Design systems**

![Storybook](https://img.shields.io/badge/Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Styled Components](https://img.shields.io/badge/Styled_Components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white)

**Backend**

![Node.js](https://img.shields.io/badge/Node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white)

**Testing & tooling**

![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Testing Library](https://img.shields.io/badge/Testing_Library-E33332?style=for-the-badge&logo=testing-library&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

**AI-native workflow**

![Claude](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=anthropic&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)

**Cloud & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_S3-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Linux](https://img.shields.io/badge/Linux_VPS-FCC624?style=for-the-badge&logo=linux&logoColor=black)

---

## What I care about

| Principle | What it means in practice |
|---|---|
| **Concepts > code** | Don't touch a line until you understand the problem. React won't save a bad data model. |
| **AI is a tool** | We direct, AI executes. The human leads — but you need to know what to ask, and why the answer might be wrong. |
| **Foundations first** | Design patterns, architecture and the DOM before frameworks. The shortcut is always longer. |
| **Write it down** | An undocumented convention isn't a convention. It's a preference you happen to have. |

---

## 📊 Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=JDavidcor23&theme=dark&hide_border=true&include_all_commits=true&count_private=true&show_icons=true" height="165" alt="GitHub stats">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=JDavidcor23&theme=dark&hide_border=true&layout=compact&langs_count=8" height="165" alt="Top languages">
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=JDavidcor23&theme=dark&hide_border=true" alt="Streak">
</p>

---

<p align="center">
  <sub>Spanish (native) · English (B2+, daily with a US-based team) · Bogotá, Colombia — remote</sub>
</p>
