<h1 align="center">Sarvesh Pingale</h1>

<p align="center">
  <b>Computer Engineering student · AI &amp; Full-Stack Developer</b><br>
  I build LLM applications, retrieval-augmented generation (RAG) pipelines, and the web backends that serve them.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/sarvesh-pingale-8b9090299"><img src="https://img.shields.io/badge/LinkedIn-Sarvesh%20Pingale-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/search?q=author%3Asarv-tech+is%3Apr+is%3Amerged&type=pullrequests"><img src="https://img.shields.io/badge/Open%20Source-Merged%20PRs-238636?style=flat-square&logo=github&logoColor=white" alt="Merged pull requests"></a>
  <img src="https://img.shields.io/badge/B.Tech%20Computer%20Engineering-2027-555555?style=flat-square" alt="B.Tech Computer Engineering, graduating 2027">
</p>

---

### About

I'm a B.Tech Computer Engineering student (graduating 2027) who likes taking an AI idea all the way to something people can actually use: a deployed app with a real interface, a clear API, and a model call that behaves predictably.

Most of my recent work sits where LLMs meet ordinary software engineering: grounding answers in a user's own documents, streaming responses without breaking the UI, handling rate limits and long conversations, and keeping secrets and model logic on the server. I also contribute to open-source projects, mostly security fixes, tests and frontend improvements.

I worked as a **Lead AI Engineer Intern at ReasonateAI Pvt. Ltd**, leading the development team building a vibe-coding platform. Previously, I completed a **Generative AI Internship at SURE ProEd**, where I developed an AI-powered code reviewer using Google Gemini 1.5 Flash and built a personal AI chatbot deployed on Streamlit.

My team was recognized as a **Local Winner and Global Nominee in the NASA Space Apps Challenge**. I was also selected for the **Aspire Leaders Program** at Aspire Institute, co-founded by Harvard Business School faculty, with resources developed in collaboration with Harvard Business School.

Beyond technology, I enjoy hackathons, networking events and continuous learning, and I'm making the most of my college journey.

I'm looking for **software engineering, AI engineering and full-stack internships**.

---

### Featured Projects

#### [NoteBot AI — Intelligent Document Retrieval System](https://github.com/sarv-tech/Intelligent-Document-Retrieval-System)
Ask questions about your own PDF notes and get answers grounded only in what the documents say.

- **Pipeline:** PyPDF2 text extraction → recursive chunking (300 chars, 50 overlap) → `BAAI/bge-small-en-v1.5` embeddings via FastEmbed → FAISS similarity search → answer generation through Groq.
- **Grounded answers:** the prompt restricts the model to retrieved context and makes it say it doesn't know when the notes don't cover the question.
- **Lightweight deployment:** FastEmbed (ONNX) replaces a PyTorch-based embedding stack so the app fits on Streamlit Community Cloud.

`Python` `LangChain` `FAISS` `FastEmbed` `Groq` `Streamlit` · [Live demo](https://intelligent-document-retrieval-system-vhgunrmheo8rycaxupxsbb.streamlit.app/)

<details>
<summary>Screenshot</summary>
<br>
<img src="https://github.com/user-attachments/assets/8ef765cc-85d9-4e0d-a071-6464f03b6f36" alt="NoteBot AI interface" width="100%">
</details>

#### [VentureGenesis — AI Startup Intelligence Platform](https://github.com/sarv-tech/VG)
*Team project*

A virtual board of directors for founders: enter startup metrics once and get risk and funding scores, a revenue forecast, and a structured debate between AI board members.

- **ML layer:** trained failure-risk and funding-readiness models with SHAP explanations, plus Prophet time-series revenue forecasting and what-if scenario simulation.
- **Multi-agent board:** a LangGraph state graph runs specialist LLM agents (investor, strategist, risk analyst and others) through a debate and produces a board decision and executive report.
- **Production structure:** FastAPI backend with SQLAlchemy, a pytest suite, Next.js 14 + TypeScript frontend with Clerk authentication, Docker, and Render / Vercel deployment config.

`Python` `FastAPI` `LangGraph` `scikit-learn` `SHAP` `Prophet` `Next.js` `TypeScript` · [Live demo](https://venture-genesis.vercel.app)

#### [MindfulMate — Conversational Wellness Companion](https://github.com/sarv-tech/MindfulMate)
A supportive chat app for everyday stress, with typed or spoken input and explicit safety rules for crisis situations.

- **Streaming chat** with Groq, keeping a sliding window of the last 10 messages so long conversations stay within the model's context limit.
- **Voice input** recorded in the browser and transcribed with Whisper (`whisper-large-v3`) before it enters the chat.
- **Robustness work:** strips model reasoning tags from the stream before display, surfaces API rate-limit (429) errors in the UI instead of failing silently, and fixes several Streamlit rendering and re-run loop issues.

`Python` `Groq` `Whisper` `Streamlit` · [Live demo](https://mindfulmate-xrz9svvq9bvq9ee7cd5fzv.streamlit.app/)

#### [AI-Powered Code Reviewer](https://github.com/sarv-tech/AI-powered-Code-Reviewer)
Paste a code snippet and get a structured review covering correctness, readability, performance and security.

- **Full-stack split:** React 19 + Vite client with a code editor and syntax-highlighted Markdown output; Node.js / Express 5 REST API (`POST /ai/get-review`).
- **Layered backend:** routes, controllers and an AI service module, with the Gemini API key kept server-side.
- **Prompt design:** a system instruction fixes the review format (summary, then issue → suggestion → explanation) so the output is consistent across languages.

`JavaScript` `React` `Vite` `Node.js` `Express` `Gemini API` · [Live demo](https://ai-powered-code-reviewer-self.vercel.app/)

<details>
<summary>Screenshot</summary>
<br>
<img src="https://github.com/user-attachments/assets/0863526b-0e20-4b11-a4a1-cf1e648619e1" alt="AI-Powered Code Reviewer demo" width="100%">
</details>

#### [Land Registry DApp](https://github.com/sarv-tech/LAND-REGISTRY-DAPP-)
An Ethereum smart contract and web interface for registering land parcels and transferring ownership on-chain.

- **Access control in Solidity:** `onlyAdmin` and `onlyVerifiedUser` modifiers; only verified users can register land and only the current owner can transfer it.
- **Auditable history:** events for user verification, registration and ownership transfer.
- **Tested:** 10 Truffle tests covering the permission rules and failure cases (duplicate registration, non-owner transfer, unregistered parcels).

`Solidity` `Truffle` `Ganache` `Web3.js` `MetaMask`

---

### Open Source

Merged contributions to community projects, mostly during **GirlScript Summer of Code 2026**:

- [**CodeGraphContext**](https://github.com/CodeGraphContext/CodeGraphContext/pull/1264) — responsive redesign of the project's comparison section.
- [**python-mini-project**](https://github.com/steam-bell-92/python-mini-project/pull/1580) — stronger directory-boundary checks in a tar extractor to block path-traversal attempts.
- [**Waggle-mcp**](https://github.com/Abhigyan-Shekhar/Waggle-mcp/pull/432) — Vitest unit tests for the Graph Studio filtering utilities.
- [**WinHome**](https://github.com/DotDev262/WinHome/pull/482) — replaced an ICMP ping connectivity check with an HTTP check that works behind corporate firewalls and VPNs.
- [**FinSight-AI**](https://github.com/AakashRathore136/FinSight-AI/pull/18) — enforced email verification before access, in both the app and backend rules.

[All merged pull requests →](https://github.com/search?q=author%3Asarv-tech+is%3Apr+is%3Amerged&type=pullrequests)

---

### Experience

**Lead AI Engineer Intern** · ReasonateAI Pvt. Ltd · Remote · Jun 2026 – Sep 2026
- Led the development team building ReasonateAI, a vibe-coding platform, focusing on AI infrastructure, LLM deployment and model integration on remote NVIDIA GPUs.
- Engineered systems that translate high-level requirements into functional frontend components, improving automation across the software development workflow.
- Contributed to AI product development for a platform serving 25K+ users, with a focus on scalable infrastructure, AI integration and usable interfaces.
- Benchmarked models and fine-tuned the open-source Qwen2.5-Coder-3B with 2-bit quantization; used RAG, LangChain and LangGraph in the backend.

**AI Trainee Intern** · SKILLFI · Remote · Jun 2026 – Jul 2026
- Assisted in the research and development of AI models and algorithms, enhancing project outcomes.
- Contributed to data collection, preprocessing and feature engineering for various AI projects.
- Collaborated with the AI team to solve complex problems and optimize model performance.
- Documented research findings and participated in team discussions to foster innovation.

**Generative AI Intern** · SURE ProEd · Remote · Dec 2024 – Jun 2025
- Gained hands-on experience in machine learning, deep learning, NLP, GANs, linear algebra and statistics.
- Used Python, the OpenAI API and Postman to develop and test LLM-based integrations and AI applications.
- Created an AI-powered code reviewer with Gemini 1.5 Flash using prompt engineering, RAG, embeddings, tokenization and APIs.
- Analyzed Kaggle diabetes datasets to train predictive machine learning models.

### Hackathons

- **NASA Space Apps Challenge 2025** · Team DataDrift · **Local Winner, Global Nominee** — Frontend Engineer on [Messier Deep Sky Navigator](https://github.com/sarv-tech/Messier-Catalog-Navigator), an interactive deep-zoom sky map of all 110 Messier objects ([live](https://messier-catalog-nasa-space-challeng.vercel.app/)).

### Leadership

**Aspire Leaders Program** · Aspire Institute · 2025
- Selected among 5,463 finalists out of 26,441 applicants in Cohort 2 of the 2025 program.
- Completed leadership development modules covering personal and professional development, strengths-based leadership, problem-solving, trust, AI, and community impact.
- Engaged with leadership and career-development resources co-created with Harvard Business School and coursework designed and delivered by Harvard faculty.

---

### Tech Stack

**Languages**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java">
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white" alt="C">
<img src="https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white" alt="SQL">
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
<img src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css&logoColor=white" alt="CSS">

**AI, ML &amp; LLM Engineering**<br>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="TensorFlow">
<img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy">
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
<img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat-square" alt="Matplotlib">
<img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face">
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangChain">
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white" alt="LangGraph">
<img src="https://img.shields.io/badge/FAISS-0467DF?style=flat-square&logo=meta&logoColor=white" alt="FAISS">
<img src="https://img.shields.io/badge/Groq-F55036?style=flat-square" alt="Groq">
<img src="https://img.shields.io/badge/Gemini%20API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini API">
<img src="https://img.shields.io/badge/RAG-555555?style=flat-square" alt="RAG">
<img src="https://img.shields.io/badge/LLMs-555555?style=flat-square" alt="LLMs">
<img src="https://img.shields.io/badge/Fine--Tuning-555555?style=flat-square" alt="Fine-Tuning">

**Web &amp; Backend**<br>
<img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">
<img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite">
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js">
<img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express">
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit">
<img src="https://img.shields.io/badge/REST%20APIs-555555?style=flat-square" alt="REST APIs">

**Databases**<br>
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB">

**Tools**<br>
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
<img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub">
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
<img src="https://img.shields.io/badge/Truffle-5E464D?style=flat-square" alt="Truffle">
<img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel">

**Engineering Practices**<br>
<img src="https://img.shields.io/badge/OOP-555555?style=flat-square" alt="Object-Oriented Programming">
<img src="https://img.shields.io/badge/SDLC-555555?style=flat-square" alt="Software Development Life Cycle">

---

### Currently

- Building LLM applications that are dependable in practice: grounded answers, streaming, and graceful handling of API limits.
- Exploring how to make RAG answers verifiable, through source citations and retrieval evaluation.
- Contributing to open-source projects, with a focus on security fixes and tests.

---

<p align="center">
  <a href="https://www.linkedin.com/in/sarvesh-pingale-8b9090299">LinkedIn</a> ·
  <a href="https://github.com/sarv-tech">GitHub</a>
</p>
