<h3 align="center">Hi, I'm Eya 👋</h3>

<p align="center">
  <b>AI &amp; Data Engineer</b>, based in Tunis, Tunisia<br>
  Engineer by training, mathematician by instinct.<br>
  I build AI systems and want to know why they work.
</p>

<p align="center">
  <a href="https://eyaazzabi.github.io/">
    <img src="https://img.shields.io/badge/Portfolio-eyaazzabi.github.io-111111?style=flat-square&logo=github&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/eya-azzabi/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:eyaazzabi04@gmail.com">
    <img src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Français-Avancé-blue?style=flat-square" alt="French">
  <img src="https://img.shields.io/badge/English-Advanced-blue?style=flat-square" alt="English">
  <img src="https://img.shields.io/badge/العربية-Native-blue?style=flat-square" alt="Arabic">
</p>

---

### About

I'm an **undergraduate engineering student at ESPRIT** (Data Science, graduating October
2027). At the same time I'm completing a **Master's in Data Science** at the University
of Carthage, and working full-time as an **AI & Backend Developer**.

I chose the second degree, and I fund it myself. I didn't want to pick between building
things and understanding them, so I took the path that gives me both: engineering
practice on one side, research depth on the other, and a job where I find out which
ideas survive contact with real users.

I came to engineering from mathematics, and that still shapes how I work. I'd rather
know *why* a model behaves the way it does than watch a metric climb. Day to day that
means LLM agents, RAG pipelines, and computer-vision systems. On my own time it means
going back to the statistics underneath them.

**I'm looking for opportunities**, in Europe
or Canada. The work I like best is the kind that ships and then has to keep working:
retrieval systems whose recall you can quote, pipelines that survive their second run,
models with error bars rather than a single flattering number.

---

### Featured work

**🌉 [JISER · جسر](https://github.com/EyaAzzabi/Jiser)** (National hackathon « IA & Finances publiques », September 2026 · **finalist**) · [live app](https://eyaazzabi.github.io/Jiser/) · [demo videos](https://eyaazzabi.github.io/Jiser/videos/)
An AI platform for Tunisian tax-reassessment disputes, linking the company that receives
a notice to every level of the tax administration, from case officer to minister.
Prototype built overnight (25–26 September 2026) with **Sarah Felah**, **Eya Rachdi** and
**Eya Idi**; ranked **2nd of 30** in the first round. Three complementary AIs: the exact
procedural rules of the tax code (8 checks), XGBoost + SHAP to score each case
(**AUC 0.84**, **+276 %** recovered when working 20 % of the backlog), and an LLM grounded
in **305 articles** through hybrid BM25 + vector retrieval, in French and Arabic.
Names and IDs are pseudonymised before any model call; data encrypted at rest.
`FastAPI` `React` `XGBoost` `SHAP` `RAG` `Supabase` `n8n` `Privacy-preserving ML`

**⚽ [Scoutable](https://github.com/EyaAzzabi/scoutable)** (OPTO Lab internship, 2026)
An AI decision-support system for football recruitment across **9,977 players** in 17
under-scouted leagues. Player-DNA embeddings in pgvector, an XGBoost model pricing what
a player *should* cost, and a ranking model blending fit, quality and value — a fix to
its normalisation lifted mean quality **+0.172** with no role below league average. The
assistant is a grounded RAG agent: it never writes SQL, routes each question to one of
seven retrieval tools, cites every player by id, and fences untrusted note text against
prompt injection. Source is private to the lab; the showcase has screenshots.
`RAG` `pgvector` `XGBoost` `LLM agents` `NestJS` `Angular`

**🔍 [rag-eval-lab](https://github.com/EyaAzzabi/rag-eval-lab)**
Everyone building with LLMs has a RAG demo; few can state their retrieval recall. This
measures it — BM25, dense vectors and rank fusion across three chunking strategies,
scored against human relevance judgments with serving cost beside every quality number.
Hybrid won everywhere (**nDCG@10 0.693**), and finer chunks turned out to help dense
retrieval while *hurting* BM25 — the two curves cross. BM25 and every metric written
from scratch.
`FAISS` `BM25` `sentence-transformers` `Evaluation` `FastAPI`

**🔬 [attention-explanation-lab](https://github.com/EyaAzzabi/attention-explanation-lab)**
An independent reproduction of *Attention is not Explanation* (Jain & Wallace, NAACL
2019), which tested BiLSTM, CNN and average encoders and **explicitly excluded
self-attention**. The reproduction holds: Kendall **τ = 0.182** and **0.204** against
the paper's 0.07–0.21 and 0.06–0.20. Extending it to the missing encoder, shuffling
attention at random moves the prediction by **0.42** without contextualisation and by
**0.0143** on a Transformer. A second extension reversed sign on the second corpus and
the mechanism I proposed for it was tested and withdrawn — both are written up rather
than deleted, along with the three bugs the tests caught.
`PyTorch` `Reproducibility` `Interpretability` `pytest` `GitHub Actions`

**🌍 [daily-climate-pipeline](https://github.com/EyaAzzabi/daily-climate-pipeline)**
A pipeline built around the problems that only appear on the *second* run: the same day
ingested twice, one source of ten failing, the API quietly returning nulls. Fourteen
quality checks run **before** the load, so a blocking failure leaves the warehouse
untouched. Runs itself every morning on GitHub Actions.
`DuckDB` `Data quality` `GitHub Actions` `ETL`

**💼 [JobReady](https://github.com/EyaAzzabi/jobready)** (Master's thesis)
A B2B staffing platform that turns unstructured CVs into queryable representations,
matches them semantically to roles, and simulates interviews with language models.
Every CV is pseudonymised with Presidio and spaCy NER **before any model call**, so the
LLM never sees who the candidate is. That implements GDPR Article 5(1)(c) in the
pipeline rather than in a policy document. Matching runs on `text-embedding-3-small`
vectors in pgvector by cosine similarity. 134-page thesis, defence autumn 2026.
`GPT-4o` `pgvector` `Presidio` `FastAPI` `NestJS` `Privacy-preserving ML`

**🌡️ [PCA of Tunisian Temperatures](https://github.com/EyaAzzabi/pca-tunisia-temperatures)**
Given only twelve monthly averages per station and no geography at all, PCA
reconstructed the two physical axes that govern Tunisian climate, explaining **98.4%**
of the variation across 16 stations. Component 1 turned out to be mean annual
temperature (r = 0.9996). Component 2 was the Mediterranean's moderating effect
(r = 0.9893). Extends my bachelor's thesis, supervised by Prof. Chaouki Aouiti.
`Python` `NumPy` `PCA`

**🦯 SenseMate.** An AI-powered device to assist visually impaired people, built as a
social-entrepreneurship project with **Enactus FSB**. I worked on it as a project
developer for 15 months, handling real-time object detection and identification with
YOLO. Won the **Early Stage award** at the Enactus National Exposition 2024.
`PyTorch` `YOLO` `IoT` `Computer Vision`

**🏛️ ArchiGuide.** An AI assistant for architectural workflows. I built the floor-plan
understanding and caption-generation models (dual-encoder CNNs, cross-attention, a
transformer decoder), fine-tuned **Phi-3 Mini with LoRA** to extract requirements from
client briefs in natural language, and helped integrate multimodal services for visual
question answering and generated architectural sketches.
`PyTorch` `LoRA` `Phi-3` `Transformers` `Computer Vision` `Generative AI`

**📡 [QoS Buddy](https://qos-buddy.vercel.app)** (live demo)
A multi-agent diagnostic platform for telecom operators. Four
autonomous agents work the network in parallel: latency and SLA-breach prediction
(Random Forest, **R² = 0.941**), trend and anomaly detection, congestion and capacity
analysis, and external context enrichment. Role-based dashboards for executive and
technical users, over roughly 8,000 records. Fourth-year integrated project at ESPRIT.
A team of 6; I contributed across data fusion, model training, LLM integration, testing
and deployment.
`Multi-agent systems` `Random Forest` `Network Analytics` `Full-stack`

**🩺 [PCOS Prediction](https://github.com/EyaAzzabi/Pcos_Prediction)**
Early detection of polycystic ovary syndrome from clinical and hormonal features.
Six models compared, from Logistic Regression through to XGBoost, with SMOTE for class
imbalance and evaluation on ROC/AUC and F1. XGBoost came out ahead.
`scikit-learn` `XGBoost` `SMOTE` `Healthcare ML`

**📧 Email Fraud Detection.** Binary classification with SVM and Random Forest over
TF-IDF features. **94% precision.**
`scikit-learn` `NLP` `TF-IDF`

**🤖 Smart Campus AI Assistant.** A hackathon build: a locally-run chatbot plus a
lost-and-found assistant that uses CLIP for image retrieval.
`NLP` `CLIP` `LLM`

---

### Currently

- 🏆 Finalist of the national hackathon « IA & Finances publiques » with **[JISER](https://github.com/EyaAzzabi/Jiser)** (final on 29 September 2026)
- 🏢 Building AI backend services at **Mafrah**: LLM integration, data pipelines, APIs
- 🎓 Finishing **JobReady**, my Master's graduation project
- 🔎 Looking for a **6-month AI/ML internship from January 2027** · Europe or Canada
- 🌍 Portfolio: **[eyaazzabi.github.io](https://eyaazzabi.github.io/)**

---

### Toolkit

| | |
|---|---|
| **Languages** | Python · SQL · R · Java · PL/SQL |
| **ML / DL** | PyTorch · scikit-learn · XGBoost · YOLO · CLIP · CNNs |
| **LLM / GenAI** | LangChain · RAG · FAISS · Chroma · agentic systems · tool-augmented AI |
| **Data** | pandas · NumPy · Spark · Hadoop · Snowflake |
| **Backend** | REST APIs · PostgreSQL · MySQL · MongoDB · Docker |
| **Stats / Viz** | PCA · inferential statistics · Matplotlib · Tableau · Power BI |

---

### Background

**ESPRIT** (École Supérieure Privée d'Ingénierie et de Technologies)
Engineering Degree, Data Science · *2025 to 2027*

**Université de Carthage, FSB**
Master's in Data Science · *2024 to present, concurrent*

**Université de Carthage, FSB**
BSc Mathematics and Computer Science · *2021 to 2024*

**Mafrah** (formerly WebFullContact) · AI & Backend Developer · *2025 to present*

**Talan Tunisie** · AI Consultant Intern · *2025*
Built intelligent agents for Connect'IS, an AI-driven sales platform.

Outside the code: I co-founded the **first youth club in Morneg, Ben Arous**, worked on
SenseMate as a project developer at **Enactus FSB**, and I'm a **Soliya Connect Program**
alumna and a speaker at **WYSE**.

---

<p align="center"><i>Arabic · French · English · a little German</i></p>
