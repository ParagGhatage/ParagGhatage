# Google Summer of Code 2025 – Final Report

**Project Title:** Perspective   
**Organization:** Aossie   
**Mentor(s):** Manav Sarkar, Pranavi Tadivalasa, Bruno    
**Contributor:** Parag Ghatage   
**GSoC Profile:** https://summerofcode.withgoogle.com/programs/2025/projects/NEioeuUn   
**GitHub Profile:** https://github.com/ParagGhatage  
**Project Repo:** https://github.com/AOSSIE-Org/Perspective  

---

## 📌 Introduction

Online media often presents information through a single lens, which can unintentionally promote bias or one-sided narratives. Readers are left without a clear understanding of counterarguments, supporting evidence, or the broader context around an issue. This lack of balanced perspectives makes it harder for people to form well-informed opinions.

Perspective addresses this challenge by providing readers with an AI-powered platform that automatically generates fact-based, structured alternative viewpoints for online articles. Using a pipeline that scrapes article content, cleans and processes text, extracts key arguments, and applies Natural Language Processing techniques with LangChain and LangGraph, the system produces logical counter-perspectives. It also integrates fact-checking by searching reliable sources and storing results in a vector database for retrieval and chat-based exploration.

The high-level goals of this project were to build a complete pipeline and frontend for user interaction, implement AI-driven alternative perspective generation, and integrate mechanisms for fact-checking and storage. By doing so, Perspective empowers readers to critically evaluate articles, reducing the impact of bias and encouraging open, balanced discussions in online communities. 

---

##  Goals of the Project

- **Develop a complete AI-powered pipeline** to scrape online articles, clean and preprocess text, extract key points, and generate well-structured counter-perspectives using LangChain and LangGraph.  
- **Build an interactive web application** with a modern frontend (Next.js + Tailwind CSS) and a robust backend (FastAPI + Python) to allow users to input article URLs and receive AI-generated alternative perspectives.  
- **Integrate fact-checking and storage mechanisms**, including automated retrieval of reliable sources for verification and a vector database for storing results and enabling efficient chat-based exploration.  

---

## 🛠️ Work Completed (Contributions)

### Pull Requests  

- [#116 – Minor code fixes](https://github.com/AOSSIE-Org/Perspective/pull/116) – General cleanup and minor bug fixes.  
- [#115 – Added docstrings and logger](https://github.com/AOSSIE-Org/Perspective/pull/115) – Improved code readability and maintainability with logging and documentation.  
- [#114 – Optimizations and formatting (frontend + backend)](https://github.com/AOSSIE-Org/Perspective/pull/114) – Enhanced performance and standardized formatting across the stack.  
- [#113 – Feat: RAG chat endpoint + Pinecone metadata fix](https://github.com/AOSSIE-Org/Perspective/pull/113) – Implemented Retrieval-Augmented Generation chat endpoint with Pinecone metadata handling.  
- [#112 – Bias checking endpoint](https://github.com/AOSSIE-Org/Perspective/pull/112) – Added API endpoint for bias detection in text.  
- [#109 – Fact check with Google Custom Search API](https://github.com/AOSSIE-Org/Perspective/pull/109) – Integrated fact-checking functionality using Google CSE.  
- [#107 – Rendering data on /results page](https://github.com/AOSSIE-Org/Perspective/pull/107) – Connected backend outputs to frontend results page for better UX.  
- [#106 – Backend deployment](https://github.com/AOSSIE-Org/Perspective/pull/106) – Configured and deployed backend to production.  
- [#105 – Store_and_send Node: Embedding & Pinecone Storage + Frontend Sync](https://github.com/AOSSIE-Org/Perspective/pull/105) – Implemented vector embeddings + Pinecone storage with frontend synchronization.  
- [#104 – Judge Perspective Node](https://github.com/AOSSIE-Org/Perspective/pull/104) – Added evaluation node to assess generated perspectives.  
- [#103 – Generate Opposite Perspective Node](https://github.com/AOSSIE-Org/Perspective/pull/103) – Created pipeline node for generating counter-perspectives.  
- [#102 – Real-time fact check functionality via Web Search + LLM](https://github.com/AOSSIE-Org/Perspective/pull/102) – Combined live search and LLM for on-the-fly fact verification.  
- [#101 – Sentiment Analysis Node using Groq SDK](https://github.com/AOSSIE-Org/Perspective/pull/101) – Integrated sentiment analysis into the pipeline.  
- [#99 – Base LangGraph setup with node files](https://github.com/AOSSIE-Org/Perspective/pull/99) – Established initial workflow structure with node architecture.  
- [#98 – Full Article Scraping Pipeline + FastAPI Integration](https://github.com/AOSSIE-Org/Perspective/pull/98) – Built scraping + preprocessing pipeline and connected it to backend.  
- [#97 – Finalized new-backend structure](https://github.com/AOSSIE-Org/Perspective/pull/97) – Organized project architecture for maintainability.  
- [#96 – Added docstrings for better readability](https://github.com/AOSSIE-Org/Perspective/pull/96) – Enhanced clarity with documentation updates.  
- [#95 – Fix: Added .npmrc in frontend for Vercel legacy peer deps issue](https://github.com/AOSSIE-Org/Perspective/pull/95) – Deployment fix for frontend on Vercel.  
- [#94 – Added .npmrc to allow legacy peer deps for deployment](https://github.com/AOSSIE-Org/Perspective/pull/94) – Solved dependency compatibility issue during deployment.  
- [#92 – Revamped frontend UI with Next.js](https://github.com/AOSSIE-Org/Perspective/pull/92) – Major UI overhaul using latest Next.js framework.  


### Features Added  

- **Full Article Scraping Pipeline** – Built a robust pipeline to scrape article content, clean text, and preprocess it for downstream AI tasks, integrated with FastAPI.  
- **Perspective Generation Nodes** – Implemented multiple LangGraph nodes including:  
  - Generate Opposite Perspective Node  
  - Judge Perspective Node  
  - Sentiment Analysis Node (via Groq SDK)  
- **Fact-Checking Mechanisms** – Added real-time fact-check functionality using Google Custom Search Engine API and integrated it with LLM-based verification.  
- **Bias Detection Endpoint** – Developed an endpoint to analyze input text for biased or one-sided narratives.  
- **Retrieval-Augmented Generation (RAG) Chat Endpoint** – Created a chat-based exploration system with Pinecone vector storage and metadata fixes for accurate retrieval.  
- **Frontend Enhancements** – Revamped the entire UI with Next.js + Tailwind CSS, built a results page for rendering data, and optimized frontend-backend sync.  
- **Deployment & Infrastructure Improvements** – Finalized new-backend structure, fixed dependency issues for Vercel deployment, and successfully deployed backend to production.  
- **Documentation & Code Quality** – Added docstrings, logging, and formatting improvements across frontend and backend for better maintainability.  


### Issues Resolved  

- **Deployment Failures on Vercel** – Fixed dependency issues by adding `.npmrc` to allow legacy peer dependencies, ensuring smooth frontend deployment.  
- **Inconsistent Backend Structure** – Finalized and reorganized the backend into a clean, modular structure for easier development and scalability.  
- **Lack of Documentation & Readability** – Resolved by adding docstrings and logging across backend modules, improving maintainability.  
- **Frontend UI/UX Gaps** – Addressed by revamping the Next.js frontend, transforming the Hero page, and rendering processed data cleanly on the `/results` page.  
- **Vector Database Integration Bugs** – Fixed Pinecone metadata issues and optimized sync between embeddings, storage, and frontend retrieval.  
  

---

##  Demo

- **Video Demo:** https://www.youtube.com/watch?v=Nq6OC8UQlLo
- **Live Deployment :** https://perspective-aossie.vercel.app  

---

##  Current State of the Project  

- **Working Features:**  
  - End-to-end pipeline for scraping online articles, cleaning text, and extracting key points.  
  - Functional LangGraph workflow with nodes for generating opposite perspectives, judging perspectives, sentiment analysis, and bias detection.  
  - Real-time fact-checking integrated with Google Custom Search API and LLM verification.  
  - Retrieval-Augmented Generation (RAG) chat endpoint backed by Pinecone vector database for context-aware conversations.  
  - Fully revamped frontend with Next.js + Tailwind CSS, including `/results` page for displaying processed outputs.  
  - Successfully deployed backend with FastAPI, ensuring stable API interaction between frontend and pipeline.  

- **Current Limitations:**  
  - Fact-checking currently depends on Google Custom Search API, which has query limits and may require alternative or additional data sources for scalability.  
  - Perspective generation is functional but may produce inconsistent quality for very complex or highly nuanced articles.  
  - Frontend lacks advanced user controls (e.g., filtering, multiple perspectives view, exporting results).

---

##  Future Work / Next Steps  

- **Enhance Fact-Checking System** – Integrate additional APIs or open-source datasets beyond Google CSE to improve reliability and reduce dependency on a single provider.  
- **Improve Perspective Generation Quality** – Fine-tune prompts, add evaluation layers, and explore model optimization to handle more complex or nuanced articles.  
- **User Experience Enhancements** – Add advanced frontend features such as filtering perspectives, multiple-perspective comparisons, exporting results (PDF/CSV), and richer visualizations.  
- **Authentication & Access Control** – Implement user accounts, authentication, and rate limiting for a more production-ready system.  
- **Scalability Improvements** – Optimize backend performance, add caching layers, and set up containerized deployment (Docker/Kubernetes) for larger-scale use.  
- **Community Contributions** – Provide contribution guidelines, improve documentation, and encourage external developers to extend LangGraph nodes or add new analysis modules.  

---

##  Challenges Faced  

- **Complex LangGraph Integration** – Designing and connecting multiple nodes (bias detection, sentiment analysis, perspective generation) into a seamless workflow required several iterations and debugging cycles to ensure stability.  
- **Fact-Checking with Limited APIs** – Relying on the Google Custom Search API introduced query limits and occasional inconsistencies, pushing me to explore hybrid approaches combining web search with LLM-based reasoning.  
- **Frontend–Backend Synchronization** – Ensuring smooth data flow between FastAPI endpoints, Pinecone storage, and the Next.js frontend was initially challenging, especially for real-time updates and rendering results.  
- **Deployment Issues** – Vercel deployment failures due to peer dependency conflicts slowed progress until I configured `.npmrc` to handle legacy deps and stabilized the CI/CD pipeline.  
- **Time & Coordination** – Balancing multiple features in parallel while syncing with mentors (Bruno, Manav, Pranavi) and other contributors required disciplined time management and clear communication.  

---

##  Learnings  

- **New Technologies Mastered** – Gained hands-on experience with LangGraph, LangChain, and Pinecone for building AI-driven pipelines; improved my skills in FastAPI for backend development and Next.js + Tailwind CSS for frontend deployment.  
- **Open-Source Collaboration** – Learned how to communicate effectively with mentors and contributors, follow structured workflows with PRs/issues, and write maintainable code with proper docstrings, logging, and clear commit histories.  
- **Practical AI Engineering** – Understood the challenges of fact-checking, bias detection, and perspective generation in real-world scenarios, including prompt design, API limitations, and ensuring logical consistency.  
- **Professional Growth** – Improved at debugging complex distributed systems, managing time across tasks, and handling deployment challenges; built confidence in contributing to a large-scale, community-focused project.  
- **Mindset Shift** – Realized that building impactful open-source AI tools is as much about *clarity and reliability* as it is about innovation.  

---

##  Resources & References

- [Project Repo](https://github.com/AOSSIE-Org/Perspective)  
- [Documentation](https://github.com/AOSSIE-Org/Perspective?tab=readme-ov-file#table-of-contents)  
- [LangChain Documentation](https://python.langchain.com/docs/)  
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)

---

## Summary of GSoC Contribution  

In this project, I designed and implemented a complete pipeline for **Perspective**, an AI-driven system that generates fact-based counter perspectives to online articles. My work covered the full stack: from building the article scraping and text-cleaning pipeline in **FastAPI**, to developing core **LangGraph nodes** (bias detection, sentiment analysis, fact-checking, and perspective generation), to integrating with **Pinecone** for vector storage and enabling chat-based exploration. On the frontend, I worked with **Next.js** and **Tailwind CSS** to provide users with a seamless interface for inputting URLs and viewing structured results.  

This work has resulted in a functional prototype that demonstrates how AI can be applied to reduce biased narratives online and empower readers with alternative viewpoints. While there are still improvements to be made (scalability, advanced fact-checking, and UI enhancements), the system is now in a state where future contributors can easily extend and refine it.  

This report, along with the code, demo video, and links above, serves as the final submission for **Google Summer of Code 2025**.  

