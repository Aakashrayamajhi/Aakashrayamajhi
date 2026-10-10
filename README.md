<div align="center">

# Aakash Jung Rayamajhi

**Software Engineer · Backend & Distributed Systems**

Building scalable, fault-tolerant systems and AI-powered automation.

[![Portfolio](https://img.shields.io/badge/Portfolio-aakashrayamajhi.com.np-0A66C2?style=flat-square&logo=googlechrome&logoColor=white)](https://aakashrayamajhi.com.np)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/aakash-rayamajhi-09b41a2a8)
[![LeetCode](https://img.shields.io/badge/LeetCode-aakashrayamajhi-FFA116?style=flat-square&logo=leetcode&logoColor=white)](https://leetcode.com/aakashrayamajhi)
[![Email](https://img.shields.io/badge/Email-aakashrayamajhi03@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:aakashrayamajhi03@gmail.com)

</div>

---

## About

Hi, I'm **Aakash Jung Rayamajhi**, a Software Engineer from Nepal and a BSc CSIT graduate (Tribhuvan University, NePathya College, 2022–2026).

I'm building myself into a **T-shaped / Pi-shaped engineer**: deep expertise in **JavaScript/TypeScript and Python**, backed by a wide working knowledge of the IT ecosystem, from backend infrastructure to mobile, cloud and AI. I like turning hard system-design problems into things that actually run: scalable, fault-tolerant and observable.

**What I build**
- **Backend & distributed systems**: microservices, event-driven pipelines with Kafka, distributed locks (Redis + ZooKeeper), search with Elasticsearch, and geo-aware services
- **Full-stack products**: MERN stack web apps and cross-platform mobile apps with React Native (Expo)
- **AI integrations & agents**: RAG systems, LLM-powered features, speech/translation pipelines, chatbots, and AI-agent workflow automation (OpenAI APIs, LangChain, n8n)
- **Reliability**: monitoring and load testing with Prometheus, Grafana, k6 and JMeter; CI/CD with Docker, Kubernetes and GitHub Actions

**What I'm doing now**
- Going deeper on system design: consistency, concurrency, caching and scaling trade-offs
- Strengthening my core in JavaScript/TypeScript and Python (DSA, backend internals, async patterns)
- Building AI agents and automation that solve real workflow problems
- Preparing to become an **open-source contributor**: reading codebases, fixing issues, shipping PRs

**Beyond the core**: I also explore the wider stack, including Next.js, NestJS, Vue, Django/FastAPI, Spring, Three.js/WebGL, Supabase/Firebase and Figma, and I enjoy experimenting, learning and building in public.

**Ask me about**: designing distributed search, preventing double-bookings with distributed locks, microservice fault tolerance, RAG pipelines, and competitive programming.

---

## Featured Projects

### SkySearch: Distributed Search Engine
Crawling → Indexing → Ranking, split into independently scalable microservices.

```mermaid
flowchart LR
    A[Crawler] -->|normalized URLs| R[(Redis dedup)]
    R --> K1{{Kafka}}
    K1 --> B[Indexer]
    B --> E[(Elasticsearch)]
    E --> C[Ranker<br/>BM25 + PageRank]
    C --> API[Search API]
    API --> UI[React UI]
```

- Scaled the 3 pipeline stages (crawl, index, rank) independently as separate microservices
- Cut redundant crawling with 2-stage dedup: URL normalization, then Redis in-memory check before queueing
- Isolated failures between services using Apache Kafka queues
- Sub-second relevance scoring with a hybrid ranker: **BM25 + PageRank** over an inverted index
- Async background workers for payload processing; Elasticsearch for retrieval

`Node.js` `Express` `React` `Kafka` `Elasticsearch` `Redis` `PostgreSQL` `Docker`

### e-Mistiri: Vehicle Servicing Platform
Microservices backend for discovering and booking vehicle service garages.

```mermaid
flowchart LR
    U[Client] --> G[Reverse Proxy / Gateway]
    G --> S1[Garage Search Svc]
    G --> S2[Booking Svc]
    G --> S3[Other Domain Svcs]
    S1 --> ES[(Elasticsearch)]
    S1 --> PG[(PostgreSQL + Geohash)]
    S2 --> L{{Redis + ZooKeeper Locks}}
    S2 --> MQ{{Message Queue}}
```

- Partitioned backend into domain microservices with isolated data stores for independent deployment
- Narrowed nearby-garage search using **Geohashing + PostgreSQL spatial indexes**
- Separated search load (Elasticsearch) from transactional load (PostgreSQL)
- Prevented double-bookings with **distributed locks** (Redis + ZooKeeper, TTL expiry)
- Improved fault tolerance with async queues, circuit breakers and reverse-proxy routing

`Node.js` `Express` `React` `MongoDB` `PostgreSQL` `Elasticsearch` `Redis` `ZooKeeper` `Docker`

> More projects and write-ups: **[aakashrayamajhi.com.np](https://aakashrayamajhi.com.np)**

---

## Tech Stack

| | |
|---|---|
| **Languages** | ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![C++](https://img.shields.io/badge/-C++-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![C](https://img.shields.io/badge/-C-A8B9CC?style=flat-square&logo=c&logoColor=black) ![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) |
| **Backend** | ![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/-Express-000000?style=flat-square&logo=express&logoColor=white) ![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white) ![WebSockets](https://img.shields.io/badge/-WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white) ![REST](https://img.shields.io/badge/-REST_APIs-009688?style=flat-square) |
| **Distributed Systems** | ![Kafka](https://img.shields.io/badge/-Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![ZooKeeper](https://img.shields.io/badge/-ZooKeeper-D22128?style=flat-square&logo=apache&logoColor=white) ![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/-Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white) |
| **Databases** | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **Cloud & DevOps** | ![AWS](https://img.shields.io/badge/-AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/-React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![React Native](https://img.shields.io/badge/-React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Expo](https://img.shields.io/badge/-Expo-000020?style=flat-square&logo=expo&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) |
| **AI & Automation** | ![OpenAI](https://img.shields.io/badge/-OpenAI_APIs-412991?style=flat-square&logo=openai&logoColor=white) ![LangChain](https://img.shields.io/badge/-LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![RAG](https://img.shields.io/badge/-RAG-FF6F00?style=flat-square) ![n8n](https://img.shields.io/badge/-n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white) ![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat-square&logo=pandas&logoColor=white) |
| **Monitoring & Testing** | ![Prometheus](https://img.shields.io/badge/-Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/-Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) ![k6](https://img.shields.io/badge/-k6-7D64FF?style=flat-square&logo=k6&logoColor=white) ![JMeter](https://img.shields.io/badge/-JMeter-D22128?style=flat-square&logo=apachejmeter&logoColor=white) |

---

## Achievements

- **National Hackathon: 2nd Runner-up**. Built speech transcription, automated translation, a RAG-based Q&A system and a WhatsApp conversational chatbot
- **Nepathon Advisor**. Guided teams on technical execution and infrastructure planning at a national hackathon
- **LeetCode Contests**. Ranked under 100 multiple times in weekly and biweekly contests
- **500+ problems solved** (300+ on LeetCode) across LeetCode, HackerRank and Codeforces
- **Esports leadership (2019–2022)**. In-Game Leader; Top 3 in FFIC 2021 Fall Open Qualifier, Top 20 in FFPL Summer 2021, representing Nepal internationally

---

## GitHub Activity

<div align="center">

<a href="https://github.com/Aakashrayamajhi">
  <img height="170" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=Aakashrayamajhi&show_icons=true&hide_border=true&theme=transparent&title_color=0A66C2&icon_color=0A66C2&text_color=8b949e&count_private=true" />
</a>
<a href="https://github.com/Aakashrayamajhi">
  <img height="170" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aakashrayamajhi&layout=compact&hide_border=true&theme=transparent&title_color=0A66C2&text_color=8b949e" />
</a>

<img alt="Contribution streak" src="https://streak-stats.demolab.com?user=Aakashrayamajhi&hide_border=true&theme=transparent&ring=0A66C2&fire=0A66C2&currStreakLabel=8b949e&sideLabels=8b949e&currStreakNum=8b949e&sideNums=8b949e&dates=8b949e" />

</div>

---

<div align="center">

**Open to internships and backend / distributed-systems roles.**
Let's build something scalable. → [aakashrayamajhi03@gmail.com](mailto:aakashrayamajhi03@gmail.com)

</div>
