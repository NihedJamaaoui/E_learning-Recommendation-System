# AI-Powered E-Learning Recommendation System with RAG

An intelligent learning platform that generates personalized quiz recommendations using **LLM agents**, **RAG (Retrieval-Augmented Generation)**, and **multi-agent orchestration** in n8n.

---

##  Key Features

✅**Multi-Agent AI System** - 4 specialized agents working in orchestration  
✅ **RAG Implementation** - Retrieves course materials before generating quizzes  
✅ **Adaptive Learning** - Personalized recommendations based on student performance  
✅ **Interactive Web Interface** - Clean React UI for students  
✅ **Explainable AI** - Transparent explanations for every recommendation  

---

## Architecture Overview

```
Student Input → Webhook → Multi-Agent Pipeline → Results Display
```

### Agent Pipeline:

1. **Learning Profiling Agent** - Analyzes student performance & categorizes knowledge levels
2. **RAG Retrieval Node** - Fetches relevant course materials from knowledge base
3. **Generative Content Agent** - Creates personalized quizzes using retrieved materials
4. **Quiz Ranking Agent** - Selects best quiz & adds correct answers
5. **Explainability Agent** - Generates friendly explanations for recommendations

---

## RAG Implementation

Our system uses **Retrieval-Augmented Generation** to ensure quiz accuracy:

- **Knowledge Base**: Course materials organized by subject and difficulty level
- **Context-Aware Retrieval**: Fetches materials matching student's knowledge level
- **Grounded Generation**: AI creates quizzes based on retrieved curriculum, not generic knowledge

**Why RAG?**  
Prevents hallucinations and ensures quizzes align with actual course content.

---

## Tech Stack

| Component | Technology |
|-----------|------------|
| **Workflow Engine** | n8n Cloud |
| **LLM Models** | OpenRouter (GPT-4 via openai/gpt-oss-120b) |
| **Frontend** | React + Tailwind CSS |
| **RAG Storage** | In-memory knowledge base (scalable to Pinecone) |
| **Integration** | Webhook API |

---

## How It Works

### 1. **Student Input**
```
Student ID: STU001
Courses: SQL, Python, JavaScript
Scores: 85, 45, 20
```

### 2. **AI Analysis**
- SQL (85) → Advanced level
- Python (45) → Intermediate level  
- JavaScript (20) → Beginner level

### 3. **RAG Retrieval**
System retrieves course materials matching each knowledge level:
- SQL Advanced: "Window functions, CTEs, Query optimization..."
- Python Intermediate: "List comprehensions, Classes, Exception handling..."
- JavaScript Beginner: "Variables, Arrays, Functions..."

### 4. **Quiz Generation**
AI creates quizzes using retrieved materials (not generic knowledge)

### 5. **Smart Ranking**
Selects the single best quiz per course + adds correct answers & explanations

### 6. **Explainability**
Generates friendly explanations:
> "We chose this SQL quiz because your score of 85 shows strong fundamentals. This advanced quiz will challenge you with window functions and CTEs."

---

## Setup Instructions

### Prerequisites
- n8n Cloud account
- OpenRouter API key
- Basic knowledge of React

### Installation

1. **Import n8n Workflow**
   - Download `workflow.json`
   - Import into n8n
   - Add OpenRouter credentials

2. **Configure Webhook**
   - Activate workflow
   - Copy production webhook URL

3. **Setup Frontend**
   - Download `index.html`
   - Update `N8N_WEBHOOK_URL` with your webhook
   - Open in browser or deploy

4. **Test**
   - Enter student information
   - Submit and view personalized recommendations!

---

## System Flow Diagram

```
┌─────────────────┐
│  Student Input  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Profiling Agent │ → Analyzes performance
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│   RAG Retrieval │ → Fetches course materials
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Content Agent  │ → Generates quizzes
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Ranking Agent   │ → Selects best quiz
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Explainability  │ → Explains choices
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Display Results│
└─────────────────┘
```

---

## Key Innovations

### 1. **Modular Agent Design**
Each agent has a single responsibility, making the system maintainable and scalable.

### 2. **RAG-First Approach**
Unlike generic quiz generators, our system grounds all content in actual curriculum materials.

### 3. **Explainability Built-In**
Students understand WHY they received specific recommendations, increasing trust and engagement.

### 4. **Adaptive Difficulty**
Quiz difficulty automatically adjusts based on demonstrated knowledge level.

---

## Use Cases

- **Educational Institutions** - Personalized assessment systems
- **Online Learning Platforms** - Adaptive quiz generation
- **Corporate Training** - Employee skill assessment
- **Self-Learning Apps** - Intelligent study recommendations

---

## Future Enhancements

- [ ] Vector database integration (Pinecone/Weaviate) for semantic search
- [ ] Support for document uploads (PDFs, DOCX)
- [ ] Real-time progress tracking dashboard
- [ ] Multi-language support
- [ ] Mobile app version
- [ ] Gamification elements

---

##  Knowledge Base Structure

Current implementation supports:
- **5 Courses**: SQL, Python, JavaScript, Java, C++
- **3 Difficulty Levels**: Beginner, Intermediate, Advanced
- **5+ Topics per level**

Easily expandable by adding to `courseDatabase` object.

---

## Contributing

This is a student project demonstrating RAG + LLM + Multi-Agent systems. 

**Potential improvements:**
- Add more course materials
- Implement vector embeddings
- Enhance UI/UX
- Add authentication

---

## Acknowledgments

- **n8n** - For the incredible workflow automation platform
- **OpenRouter** - For LLM API access
- **Anthropic** - For AI assistance in development

---

## Academic Context

**Project Type**: E-Learning AI System  
**Key Concepts**: RAG, Multi-Agent Systems, LLM Orchestration, Adaptive Learning  
**Technologies**: n8n, React, OpenRouter, Tailwind CSS

**Learning Outcomes:**
- Implemented production-ready RAG system
- Orchestrated multiple LLM agents
- Built end-to-end AI application
- Applied AI ethics (explainability, transparency)

---

⭐ **If you found this helpful, please star the repository!**

#AI #MachineLearning #RAG #Education #n8n #React #LLM #AdaptiveLearning
