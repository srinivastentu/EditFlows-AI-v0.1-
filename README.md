# 🎬 EditFlows AI
The capstone project in the category of "AI in Film Editing" for the course "Minor in AI" from IIT-Ropar.

**AI-Assisted Editorial Intelligence for Film & Video Editing**
EditFlows AI is an AI-assisted film editing system that generates **editorially reasoned first cuts** from raw footage by combining story intent, audio–visual understanding, continuity logic, and deterministic editorial personas.
It is designed as a **decision-support tool for professional editors**, not a replacement for human creativity.

---

## ✨ Key Idea
> **AI understands → human corrects → AI edits → human reviews → AI re-edits → human approves → exports to Premiere Pro**
EditFlows AI treats **editorial understanding as a first-class artifact**, allowing editors to inspect and refine AI reasoning *before* any edit is generated.

---

## 🚀 Core Features (MVP)
* **AI Understanding Layer**
  * Story intent, scenes, emotional arc
  * Dialogue grammar & audio continuity
  * Spatial & visual continuity reasoning
  * Performance timing & cut motivation validation

* **Multiple Editorial Personas**
  * Narrative-driven
  * Emotion-driven
  * Rhythm / pace-driven

* **Professional Workflow**
  * Raw footage ingestion (up to 50 clips)
  * ProRes 422 transcoding for editing
  * H.264 previews for fast review
  * Premiere Pro XML export

* **Human-in-the-Loop Control**
  * Editors can review and edit AI understanding artifacts
  * No automatic final decisions without human approval

---
## 🧠 AI Techniques Used

* **LLMs (Inference only, no training)**
  * Anthropic Claude (editorial reasoning)
  * OpenAI Whisper (speech-to-text)
  * OpenAI GPT-4o Vision (visual understanding)

* **Media Processing**
  * FFmpeg (transcoding, audio extraction)
  * MoviePy (preview assembly)

---

## 🏗️ System Architecture (High-Level)

```
Raw Footage
   ↓
Transcode (ProRes / H.264)
   ↓
Ingest + Audio Extraction
   ↓
AI Analysis (Audio + Visual)
   ↓
Editorial Understanding Artifacts (JSON)
   ↓
Edit Flow Generation (Personas)
   ↓
Preview Rendering
   ↓
Premiere Pro XML Export
```

---
## 🛠️ Prerequisites

| Requirement       | Notes                                          |
| ----------------- | ---------------------------------------------- |
| FFmpeg            | Must be installed and available in system PATH |
| Python 3.10+      | Required                                       |
| Node.js           | For UI prototype                               |
| Anthropic API Key | `ANTHROPIC_API_KEY`                            |
| OpenAI API Key    | `OPENAI_API_KEY`                               |
| Raw Footage       | MP4 / MOV / MXF (max 50 clips)                 |

---

## 📂 Project Structure (Simplified)
```
EditFlows-AI/
│
├── src/
│   ├── transcode.py
│   ├── ingest.py
│   ├── analyze.py
│   ├── edit.py
│   ├── api_server.py
│
├── data/
│   └── processed/
│       ├── clips_registry.json
│       ├── story_intent.json
│       ├── scenes.json
│       ├── spatial_continuity.json
│       ├── dialogue_grammar.json
│       ├── edit_flows.json
│       └── premiere_export/
│
├── media/
│   ├── editorial/
│   ├── preview/
│   └── media_map.json
│
├── ui_prototype/
│
└── README.md
```

---
## 🧪 Typical Workflow

1. **Organize raw footage**
2. **Transcode to editorial formats**
3. **Run ingestion & AI analysis**
4. **Manually define story intent**
5. **Generate edits via UI**
6. **Review previews**
7. **Export Premiere Pro XML**
8. **Refine edit in Premiere Pro**

---

## 🎯 Design Philosophy
* AI assists, **editors decide**
* Transparency over automation
* Deterministic, explainable edit logic
* Professional post-production compatibility
* No black-box editing

---

## ⚠️ Limitations (MVP)
* No learning across projects
* No multi-user collaboration
* No automatic final cut approval
* No long-term edit history tracking

---

## 🔮 Future Scope
* Adaptive learning from editor feedback
* Deeper performance analysis
* Multi-editor collaboration
* Expanded NLE support
* Full AI Film Studio pipeline (script → edit → sound)

---

## 🧑‍⚖️ Ethics & Responsible AI
* No model training on user data
* All AI decisions are reviewable
* No personal data retention
* Human approval required for all exports

---
## 📜 License

This project is intended for **academic, research, and experimental use**.
Commercial use and redistribution are subject to future licensing decisions.

---

## 🙏 Acknowledgements
Developed as part of the **Minor in AI** program
**IIT Ropar × Masai**

Just tell me the next step.
