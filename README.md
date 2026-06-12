# G Yeshwanth Kumar Reddy

**Full Stack & AI/ML Developer | Founder [botplexus.com](https://botplexus.com) | Freelancer**

Building production-grade AI systems, SaaS platforms, and agentic workflows for clients across India, the US, and Europe. Started freelancing in my 2nd year of college. Currently running a live B2B SaaS product.

---

## About Me

I'm a 21-year-old developer from, India. I taught myself frontend first, then moved into full-stack, and eventually into AI/ML and LLM engineering. While doing freelance work, I noticed that the AI chatbots on most company websites gave robotic, repetitive answers with zero real understanding of the business. That frustration became BotPlexus.

I do not just build for side projects. Every system I ship has real users, real traffic, or a real client behind it.

- Founder of **BotPlexus** - a no-code B2B SaaS for AI-powered customer support
- Part-time developer at **Bodhasoft** - building production apps with 500+ active users
- Freelancer for **national and international clients** - US, Europe, India
- 2+ years of industry experience before graduating in 2026

---

## Platform Metrics (Real Usage)

- **BotPlexus** - Live at [botplexus.com](https://botplexus.com)
  - No-code AI chatbot SaaS, deployed on GCP Cloud Run
  - RAG-based Q&A mode + Agentic mode with 90+ integrations
  - Razorpay payment infrastructure, stackable query packs
  - Early customers onboarded

- **Bodhasoft - Gamified Coding Workspace**
  - 500+ active students across multiple institutions
  - 10,000+ daily API requests, sub-300ms response times

- **Go2Resume (Freelance - US Client)**
  - AI-powered ATS-optimized resume builder
  - Delivered end-to-end, paid $1,000 USD

- **Cosmetic Brand Automation (Freelance - Pune Client)**
  - 12 agentic workflows, 78 agents total
  - Covers operations, marketing, sales, R&D, and executive functions
  - Designed to automate ~80% of business processes

---

## BotPlexus - Architecture

BotPlexus is a multi-tenant no-code SaaS that lets any business build, train, and deploy AI chatbots without ML expertise.

**Two chatbot modes:**

```
FAQ / Q&A Mode                          Agentic Mode
--------------------                    ----------------------
[ Business uploads docs/FAQs ]          [ Business connects APIs/tools ]
          |                                       |
          v                                       v
  [ RAG Ingestion Pipeline ]            [ Agent + Tool Config ]
  (chunk -> embed -> store)                       |
          |                             [ LangGraph Agent Runtime ]
          v                                       |
  [ pgvector / FAISS Store ]            [ Tool Router & Executor ]
          |                                       |
          v                                       v
  [ Retriever -> LLM -> Response ]      [ Multi-step reasoning + action ]
          |                                       |
          v                                       v
  [ Embed on website / app ]            [ Embed on website / app ]
```

**Self-Healing RAG Pipeline (LangGraph):**

```
[ User Query ]
      |
      v
[ Retriever ]
      |
      v
[ Generator (LLM) ]
      |
      v
[ Critic Agent ] ---- passes? ----> [ Final Response ]
      |
   fails?
      |
      v
[ Retry with reformulated query ] (max 3 attempts)
      |
      v
[ Generator ] -> [ Critic Agent ] -> [ Final Response ]
```

**Multi-Tenant Infrastructure:**

```
[ Tenant A ] [ Tenant B ] [ Tenant C ]
      |             |             |
      v             v             v
  [ API Gateway (FastAPI) ]
              |
    ----------------------
    |                    |
[ RAG Engine ]    [ Agent Engine ]
    |                    |
[ pgvector DB ]   [ LangGraph Runtime ]
    |                    |
    ----------------------
              |
     [ GCP Cloud Run ]
              |
     [ HTTPS / SSL ]
```

---

## Agentic Workflow Architecture (Cosmetic Brand Client)

Built for a Pune-based cosmetic brand to automate ~80% of business operations using chained multi-agent pipelines.

```
[ Trigger Layer ]
  Scheduled / Event-based / Manual
          |
          v
[ Workflow Router ] (12 Workflows)
  |        |        |        |
  v        v        v        v
[Ops]  [Marketing] [Sales] [R&D]   ... 8 more
  |        |        |        |
  v        v        v        v
[ Domain Agents ] (78 agents total)
  - Output of Agent N -> Input of Agent N+1
  - Each agent is scoped, tool-equipped, memory-aware
          |
          v
[ Output Layer: Reports / Actions / Notifications ]
```

---

## Tech Stack

### Frontend
- React.js, Next.js, React Native
- TypeScript, Tailwind CSS, Figma

### Backend
- Node.js (Express.js), FastAPI, Spring Boot, Flask, Django
- RESTful APIs, MERN Stack

### AI / ML
- LangChain, LangGraph, RAG Pipelines
- LLMs: GPT, Gemini, Claude APIs
- Vector DBs: pgvector, Pinecone, FAISS
- TensorFlow, PyTorch, Hugging Face
- NLP, Computer Vision, Deep Learning

### Databases
- MongoDB, PostgreSQL, MySQL, Supabase, Neon

### Cloud & DevOps
- GCP (Cloud Run), AWS (EC2, S3, Lambda, RDS)
- Docker, GitHub Actions, CI/CD

### Automation
- n8n, Zapier, Microsoft Power Automate, Agentforce (Salesforce)

---

## Featured Projects

### BotPlexus
No-code B2B SaaS for AI-powered customer support chatbots. Multi-tenant, RAG-based, with agentic mode and 90+ integrations. Live at [botplexus.com](https://botplexus.com).

### Go2Resume
AI-powered resume generation platform. Builds tailored, ATS-optimized resumes using LLMs and dynamic user input. Delivered for a US-based client.

### Lexion
LinkedIn-style professional networking platform built specifically for lawyers. Connects junior and senior advocates, includes structured courses and mentorship tools. Built as CTO/Chief Architect.

### Agri-Responses
Full-stack agricultural advisory web app with a React/Vite frontend and dual Node.js + FastAPI backend. Integrates Gemini AI to answer farmer queries intelligently.

### Smart Hostel Management System
AI-powered hostel administration platform with face recognition attendance (DeepFace), NLP chatbot, and real-time analytics. Built with React, Flask, and MySQL.

### At-Risk Student Detection
ML system that analyzes academic, behavioral, and attendance data to proactively identify students at risk of dropout or failure.

### Driver Drowsiness Detection
Real-time alertness monitoring using computer vision and facial landmark analysis. Detects drowsiness and triggers safety alerts.

---

## Professional Experience

**Full Stack Developer with AI Integration - Bodhasoft** (2023 - Present)
- Built 5+ production applications serving 500+ active users
- 10,000+ daily API requests with sub-300ms response times
- Deployed on AWS EC2, GCP, and Render with CI/CD pipelines
- RAG pipelines with 85%+ retrieval accuracy

**Freelance Full Stack & AI/ML Developer** (2024 - Present)
- Clients across India, US, and Europe
- Domains: education, legal-tech, e-commerce, cosmetics, enterprise
- Started as UI/UX, expanded to backend, full-stack, then AI/ML

---

## Certifications

- TensorFlow Developer Certificate - Google, 2025
- AWS Certified Cloud Practitioner - Amazon Web Services, 2024
- Meta Front-End Developer Professional Certificate - Meta, 2023
- Full Stack Experience Certificate - Bodhasoft, 2025
- AI & ML Internship Certification - Skill Intern, 2024

---

## Achievements

- Completed Agentforce Hackathon by Salesforce (2026), building an AI-powered agent on the Salesforce platform
- Collaborated with IIT Bombay students on joint technical projects
- Delivered software for clients across healthcare, legal-tech, education, and enterprise
- Built a production coding workspace used by 500+ students across multiple institutions

---

## Engineering Philosophy

- Real users beat perfect architecture. Ship, observe, iterate.
- AI features should solve a real workflow problem, not just exist.
- Every layer of the stack should be something I can debug end to end.
- Reading every project brief carefully is how you understand what the world actually needs.

---

## Connect

- Portfolio / SaaS: [botplexus.com](https://botplexus.com)
- LinkedIn: [linkedin.com/in/yeshwanth-kumar](https://www.linkedin.com/in/yeshwanth-kumar-reddy-a6a27334b)
- GitHub: [github.com/Yeshwanthhhh2005](https://github.com/Yeshwanthhhh2005)
- Email: yeshwanthkumarr2004@gmail.com

---

> I started reading project descriptions as a freelancer to figure out what clients needed. That habit turned into a lens for understanding what the world actually lacks. That is what I build toward.
