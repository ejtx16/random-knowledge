---
Date: 2025-09-28 - 2026-10-06
Tags: "#AI #LLM #Agents #RAG #ClaudeCode"
---

# AI Knowledge Base

A curated collection of AI concepts, tools, workflows, and practical notes gathered from across this vault, explained in one sentence each for beginners and professionals.

---

## Table of Contents

- [AI Fundamentals](#ai-fundamentals)
- [Machine Learning](#machine-learning)
- [Large Language Models](#large-language-models)
- [Prompt & Context Engineering](#prompt--context-engineering)
- [Embeddings, Vector Databases & RAG](#embeddings-vector-databases--rag)
- [AI Agents & Agentic Workflows](#ai-agents--agentic-workflows)
- [Model Context Protocol (MCP)](#model-context-protocol-mcp)
- [Agent Context Sources](#agent-context-sources)
- [AI Security](#ai-security)
- [AI-Assisted Development](#ai-assisted-development)
- [Claude Code](#claude-code)
- [Learning with AI](#learning-with-ai)
- [Content Ideas](#content-ideas)
- [References](#references)

---

## AI Fundamentals

- **Generative AI (GenAI)** - AI that creates new content such as text, images, code, or sound instead of only analyzing existing data.
- **Predictive AI** - AI that uses patterns in past data to forecast an outcome, like a price, a label, or a risk score.
- **NLP (Natural Language Processing)** - the field of teaching computers to read, understand, and produce human language.
- **GPT (Generative Pre-trained Transformer)** - a model family that is pre-trained on huge amounts of text and then generates text one token at a time using the transformer architecture.
- **GANs (Generative Adversarial Networks)** - two neural networks trained against each other, where a **generator** makes fake samples and a **discriminator** tries to tell them apart from real ones until the fakes become convincing.
- **Symbolic AI** - AI built from explicit, hand-written rules and logic that a human can read and trace.
- **Sub-symbolic AI** - AI that learns behavior through numeric calculation in neural networks loosely inspired by neurons in the brain, rather than from written rules.
- **AGI (Artificial General Intelligence)** - a hypothetical AI that can learn and perform any intellectual task a human can.
- **ASI (Artificial Super Intelligence)** - a hypothetical AI that surpasses the best human ability in practically every domain.

---

## Machine Learning

- **Machine Learning (ML)** - a branch of AI where algorithms learn patterns from training data so they can make predictions without being explicitly programmed.
- **Deep Learning** - a subcategory of ML that uses many-layered neural networks to learn complex patterns such as images, speech, and language.
- **Neural Network** - a model architecture made of connected layers of "neurons" that adjust numeric weights during training to recognize patterns.
- **Garbage In, Garbage Out** - an ML model can only be as good as its training data, so quality data matters more than clever algorithms.

**Learning Types:**


| Type             | Explanation                                                                                       |
| ---------------- | ------------------------------------------------------------------------------------------------- |
| **Supervised**   | The model learns from labeled examples, mapping inputs (x) to known outputs (y).                  |
| **Unsupervised** | The model finds hidden patterns or groups in unlabeled data on its own.                           |


**Top 3 ML Tasks:**


| Task               | Explanation                                                                  |
| ------------------ | ---------------------------------------------------------------------------- |
| **Classification** | Predicts which category something belongs to, such as spam or not spam.      |
| **Regression**     | Predicts a continuous number, such as a house price or temperature.          |
| **Clustering**     | Groups similar data points together without being told the groups in advance. |


**Common Algorithms & Techniques:**

- **Linear Regression** - fits a straight line through data points to predict a number from one or more inputs.
- **Logistic Regression** - uses an S-shaped curve to output a probability between 0 and 1, which makes it a classification method despite its name.
- **Decision Tree** - makes predictions by asking a series of yes/no questions arranged in a tree structure.
- **Elbow Method & Silhouette Score** - two ways to pick the best number of clusters, by finding where adding more clusters stops helping (elbow) or how well each point fits its cluster (silhouette).
- **Ensemble Learning** - combines several base models so their joint prediction is more accurate than any single one.
- **Bagging** - trains many models in parallel on random samples of the data and averages or votes on their predictions.
- **Stacking** - feeds the predictions of several models into a final model that learns how best to combine them.
- **Boosting** - trains models one after another, with each new model focusing on the mistakes of the previous ones.

---

## Large Language Models

- **LLM (Large Language Model)** - a very large neural network trained on massive text data that acts as a reasoning engine able to understand and generate language.
- **The Three Ingredients** - an LLM's ability comes from its training data, its model architecture, and how it is trained.
- **Transformer** - the neural network architecture behind modern LLMs that uses "attention" to weigh how every word in the input relates to every other word.
- **Next-Token Prediction** - an LLM generates text by repeatedly predicting the most likely next token based on everything before it.
- **Tokens** - the small chunks of text (words or word pieces) that a model reads and writes, and that usage and pricing are measured in.
- **AI Models = API Endpoints** - in practice most apps use a model by sending a request to a provider's API endpoint and receiving a response.
- **Hallucination** - when a model confidently produces false or made-up information, usually caused by poor data quality, the generation method, or missing input context.
- **Active Mitigation** - reducing hallucinations by giving clear, specific prompts, supplying trusted context, and verifying the output.
- **Fine-Tuning** - further training a pre-trained model on a smaller, focused dataset so it performs better in a specific domain.
- **Supervised Fine-Tuning (SFT)** - fine-tuning with labeled examples of the desired input and output so the model learns a domain-focused behavior.
- **MoE (Mixture of Experts)** - an architecture where many specialized neural sub-networks ("experts") exist and only the most relevant ones are activated for each input, saving compute.
- **LRM (Large Reasoning Model)** - an LLM trained to think through problems step by step before answering, trading speed for better accuracy on hard tasks.
- **Common Uses** - LLMs power intelligent chatbots, content creation, and software development.

---

## Prompt & Context Engineering

- **Prompt Engineering** - the practice of writing clear instructions for an AI so it produces the result you actually want.
- **Specific Prompts Win** - the more specific your prompt is, the more accurate the result, because the model has less to guess.
- **Multi-Shot Prompting** - including several examples of the desired input and output in the prompt so the model copies the pattern.
- **Hard Prompts vs. Soft Prompts** - hard prompts are human-written text instructions, while soft prompts are learned numeric embeddings that steer a model and are created through prompt tuning.
- **System Prompt** - the background guidelines given to a model before the conversation that define its role, rules, and behavior.
- **Context Engineering** - the discipline of deciding what information goes into a model's context window, when, and in what form, so the model has exactly what it needs.
- **Context Rot** - adding more and more context does not always help, because model quality degrades as the context gets long and cluttered.
- **Context Processing & Management** - cleaning, summarizing, and organizing information before and during a session so the context stays useful.
- **Writing Is Thinking** - writing your own ideas first clarifies your thinking, and LLMs work best as tools to expand and edit that thinking rather than replace it.

**What Makes Good Context:**


| Quality         | Explanation                                                                     |
| --------------- | ------------------------------------------------------------------------------- |
| **Relevance**   | Include only information that matters to the current task.                      |
| **Structure**   | Organize information clearly with headings, lists, or sections so it is easy to use. |
| **Timing**      | Provide information at the moment it is needed rather than all upfront.         |
| **Compression** | Summarize long material so it keeps the meaning while using fewer tokens.       |


---

## Embeddings, Vector Databases & RAG

- **Embedding** - turning text (or images) into a list of numbers (a vector) so that items with similar meaning end up close together.
- **Embedding Space** - the multi-dimensional space where vectors live, and where distance between vectors represents difference in meaning.
- **Embedding Model** - a model whose only job is to convert text into vectors, such as the free Hugging Face `all-MiniLM-L6-v2`.
- **Vector Database** - a database built to store vectors and quickly find the ones most similar to a query vector.
- **RAG (Retrieval-Augmented Generation)** - a technique that extends a model's knowledge by retrieving relevant passages from your own documents and adding them to the prompt before the model answers.
- **Retrieval / Augmented / Generation** - *retrieval* finds the relevant information, *augmented* adds it to the prompt, and *generation* writes the answer from that context.
- **Chunking** - splitting large documents into small pieces so only the relevant parts are sent to the model instead of overloading its context.
- **Chunk Size** - the maximum number of characters allowed in each chunk.
- **Chunk Overlap** - the number of characters shared between neighboring chunks so a sentence cut in half keeps its meaning in at least one chunk.
- **Similarity Search (Top-k)** - finding the *k* chunks whose vectors are closest to the question, such as the top 3, and passing them to the model.

**The RAG Pipeline:**

```
Load document -> Split into chunks -> Embed chunks -> Store in vector DB
Query -> Embed query -> Similarity search (top-k) -> Add chunks to prompt -> LLM answers
```

---

## AI Agents & Agentic Workflows

- **LLM → reasoning engine** - the model is the "brain" that thinks but cannot act on its own.
- **Agent → LLM + ability to take actions** - an agent is a prompt, an LLM, and a set of tools that let it act autonomously toward a goal.
- **Agentic Harness** - the system around an agent that manages its actions, tools, context, execution loop, and guardrails.
- **Agent Loop** - agents work in a repeating cycle of perceive → reason → act → observe until the goal is reached.
- **Agent Flow** - a typical agent breaks a goal into steps, uses tools to retrieve information, and stores what it learns in memory.
- **Tool Descriptions** - an agent decides when to call a tool by reading the tool's description, so clear descriptions lead to correct tool use.
- **Orchestrate and Verify** - the human's role shifts from writing every line to directing agents and checking their output.
- **Agentic Eval** - systematically testing an agent's outputs and behavior against expected results to measure how reliable it is.
- **ADLC (Agent Development Lifecycle)** - the end-to-end process of designing, building, testing, deploying, and monitoring AI agents.

**Agentic Workflow Types:**


| Type                         | Explanation                                                        | Frameworks               |
| ---------------------------- | ------------------------------------------------------------------ | ------------------------ |
| **Linear**                   | Fixed, predictable steps run in order, often for data pipelines.   | LangChain, LlamaIndex    |
| **Autonomous**               | The agent pursues an open-ended goal and plans its own steps, as in coding agents. | AutoGen, BabyAGI, CrewAI |
| **Role-based**               | Multiple agents with defined roles collaborate like a team.        | AutoGen, CrewAI, ChatDev |
| **Production orchestration** | Agents wired into real development and business systems with control and reliability. | LangGraph, Agent Framework |
| **Rapid prototyping**        | Visual, low-code builders used to validate ideas quickly.          | Langflow, Flowise        |


**Agent Failure Modes:**

- **Infinite Loop** - the agent keeps repeating the same steps without making progress or stopping.
- **Hallucinated Plan** - the agent confidently follows a plan built on false assumptions or nonexistent facts.
- **Unsafe Tool Use** - the agent runs a tool in a harmful way, such as deleting data or leaking secrets.

---

## Model Context Protocol (MCP)

- **MCP (Model Context Protocol)** - an open standard that lets AI apps connect to external tools and data sources through one common interface, acting as the orchestration layer between models and apps.
- **The Flow** - the LLM talks to an MCP server, and the MCP server talks to the actual apps or data sources.
- **Client/Server Model** - the AI app runs an MCP client that connects to one or more MCP servers, each exposing a specific capability.
- **Tools** - actions an MCP server lets the model perform, such as searching, creating a file, or sending a message.
- **Resources** - data an MCP server exposes for the model to read, such as files, records, or documents.
- **Prompt Templates** - reusable, pre-written prompts that an MCP server offers for common tasks.
- **MCP Server Wraps an API** - an MCP server is often a thin wrapper around an existing API, making that source usable by any MCP-compatible AI.
- **Dynamic Self-Discovery** - an MCP client can ask a server what it offers at runtime, so the model learns available tools without hard-coding them.

**API vs. MCP:**


| API                                              | MCP                                                                |
| ------------------------------------------------ | ------------------------------------------------------------------ |
| Purpose-built for one specific integration.      | General-purpose standard interface for any AI app.                 |
| Each integration is coded and maintained separately. | Abstraction that simplifies integration across many sources.    |
| Capabilities are fixed in documentation.         | Capabilities are discovered dynamically at runtime.                |


---

## Agent Context Sources

To do good work, an agent first needs to gather all the right context:


| Source     | Explanation                                                                    |
| ---------- | ------------------------------------------------------------------------------ |
| **Skills** | Repeatable, written instructions the agent loads when a task matches.          |
| **MCP**    | Pulls in live context from external tools and systems.                         |
| **Memory** | The agent's saved experience, such as preferences and past decisions.          |
| **RAG**    | Written knowledge stored in documents that can be searched and pulled in on demand. |


---

## AI Security

- **Non-Human Identity (NHI)** - AI agents and services need their own credentials and identities, which must be managed just as carefully as human accounts.
- **Just-in-Time (JIT) Access** - granting permissions only at the moment they are needed and removing them afterward, so standing access cannot be abused.
- **RBAC (Role-Based Access Control)** - permissions are assigned to roles rather than individuals, so an agent can only do what its role allows.
- **Audit** - logging every action an agent takes so it can be reviewed, traced, and investigated later.
- **AI Firewall / Proxy / Gateway** - a control layer between users, agents, and models that filters requests and responses to block attacks and data leaks.

**The Art of War Applied to Security:**


| Principle             | Security Practice                                                                 |
| --------------------- | --------------------------------------------------------------------------------- |
| **Know self & enemy** | Threat intelligence reveals who attacks you and how.                              |
| **Win before you fight** | Patching, hardening, MFA/passkeys, and Zero Trust stop attacks before they start. |
| **Deception**         | Honeypots lure attackers into fake systems to expose them.                        |
| **Speed & adapt**     | Shrink the time from identifying an incident (MTTI) to containing it (MTTC).       |
| **Prioritize**        | Risk analysis focuses limited effort on the threats that matter most.             |
| **Position**          | Extensive monitoring gives visibility across every part of the system.            |
| **Leadership**        | Someone must own and lead the security effort.                                    |


---

## AI-Assisted Development

### Top 3 AI Usages

1. **Automate** - use AI to automate manual or lengthy processes that are data-heavy.
2. **Draft** - use AI to create the first draft of any business idea or decision.
3. **Coding Buddy & Architect** - use AI as a pair programmer and software architect to understand the best trade-offs when building an app.

### 3 Essential Developer Skills in 2026

1. **Think Like an Architect** - understand the nature of the system, its data flow, and how small components connect into larger ones.
2. **Connect Code to the Business** - your job is to build products that create value by reducing costs or generating revenue, not just to write code.
3. **Leverage AI** - use AI as a tool to automate tasks and as a guide for any topic or idea you need.

### How Cursor Works

- **Composer Agent** - Cursor's agent receives your query and chooses tools such as Read File, Edit File, Codebase Search, Collect Lints, and Terminal Command to complete the task.
- **Sub-agents** - helper agents that handle specialized sub-tasks so the main agent stays focused.

### Workflow Modes


| Mode          | Explanation                                         |
| ------------- | --------------------------------------------------- |
| **Research**  | Gather context and understand the problem first.    |
| **Plan**      | Design the approach and surface decisions before coding. |
| **Implement** | Let the agent execute the agreed plan.              |


Equivalent in Cursor: **Ask -> Plan -> Agent**

Practical loop: **Plan mode -> Edit specs -> Run agent**

### You Are the Driver When Using AI

1. **Surface decisions** - identify which choices need to be made.
2. **Understand trade-offs** - weigh the pros and cons of each option.
3. **Make choices** - decide consciously and record your reasoning.

### Recommended AI Model Usage


| Model         | Best For            |
| ------------- | ------------------- |
| Opus          | Coding (most tasks) |
| GPT-5.3 Codex | Debugging           |
| Gemini Pro 3  | UI/UX               |
| Composer 2    | Testing             |


### Document Flow for AI-Built Projects

1. **Surface, Explore, Record** - list the business decisions, check their strengths, weaknesses, and trade-offs, then write them down.
2. **BRD (Business Requirements Document)** - explains *why* we build it, based on the business overview and user journey.
3. **PRD (Product Requirements Document)** - explains *how* we can build it.
4. **Design Requirements Document** - defines how the product should look and behave.
5. **ADRs (Architecture Decision Records)** - record each technical decision, the options considered, and why one was chosen.

### Productivity Principles

1. **Automate** - let tools handle repetitive work so you focus on what matters.
2. **Design first, experiment later** - plan the shape of the solution before trying things.
3. **Flow state** - protect long, uninterrupted blocks of focused work.
4. **Lessen the cognitive load** - keep systems simple so less needs to be held in your head.
5. **Make room for growth** - leave time and space to learn new skills.
6. **Use modern tools** - adopt tools that make you faster and better.

Measure results by **Speed, Quality, Effectiveness, and Impact**, and remember that what wins is **taste, distribution, and something people want**.

### Testing & Release Practices

- **Feature Gating** - hiding new features behind flags so they can be turned on gradually or switched off instantly.
- **Mutation Testing** - deliberately introducing small bugs into code to check whether your tests catch them, which measures test quality.

---

## Claude Code

- **Claude Code (CC)** - Anthropic's agentic coding tool that runs in your terminal, reads your codebase, edits files, and runs commands for you.
- **Ask About the Codebase** - you can ask Claude Code questions about an unfamiliar codebase to understand it quickly.
- **CLAUDE.md** - a project instructions file that Claude Code reads at the start of every session so it follows your conventions.
- **Built-in Agents (Subagents)** - specialized helper agents Claude Code can launch to handle focused sub-tasks in their own context.
- **Caveman Mode** - a plugin that makes Claude respond in very short, compressed sentences to save tokens.

**Installation:**

```bash
# Install Claude Code globally
npm install -g @anthropic-ai/claude-code

# Start Claude Code in your project folder
claude

# Inside Claude Code, sign in to your Anthropic account
/login
```

**Underrated Commands:**


| Command     | Explanation                                                                 |
| ----------- | --------------------------------------------------------------------------- |
| `/resume`   | Returns to an earlier conversation by ID or name, or opens the session picker. |
| `/rewind`   | Rolls code and conversation back to a previous checkpoint.                  |
| `/recap`    | Generates a one-line summary of the current session on demand.              |
| `/insights` | Generates an HTML report analyzing how you use Claude Code across recent sessions. |
| `/btw`      | Asks a side question about the session without adding it to the conversation history. |
| `/init`     | Creates a starter `CLAUDE.md` guide for the project.                        |


---

## Learning with AI

### Learning Anything Using Obsidian, Gemini, and Cursor

1. **Research** - ask Gemini Deep Research for a learning roadmap, such as *"Create a 30 day boot camp learning roadmap for the fundamentals of web development with links"*, then export it as a Markdown file.
2. **Generate topic files** - open the Markdown file in Cursor and ask it to create one file per topic, each with an introduction and knowledge points written as `[[wikilinks]]`.
3. **Build the roadmap** - ask Cursor to add every generated file name under its matching topic in the roadmap file using `[[]]`, so the whole roadmap is linked in Obsidian.

---

## Content Ideas

- **Simple RAG with Claude Code and Obsidian** - show how to use your notes vault as a searchable knowledge base for AI.
- **What Is an Agent Harness** - explain the system that manages an agent's tools, context, and guardrails.
- **Local LLMs for n8n Automations** - run a model on your own machine to power workflow automations privately.
- **How to Use Cursor Effectively** - cover multitasking and getting better results when coding with AI.
- **Copilot** - compare GitHub Copilot with other AI coding assistants.
- **Knowledge Base for Beginners** - build simple notes that explain AI concepts for newcomers.
- **CLAUDE.md from Scratch** - walk through writing a project instructions file for Claude Code.

---

## References

### Videos


| Topic                       | Link                                                                 |
| --------------------------- | -------------------------------------------------------------------- |
| AI Agents                   | [YouTube](https://www.youtube.com/watch?v=g24tJk8Flsk)               |
| RAG Pipeline Tutorial       | [YouTube](https://www.youtube.com/watch?v=g8FIfgKYtyI)               |
| Vector Databases            | [YouTube](https://www.youtube.com/watch?v=VVNYQKDLY5s&t=49s)         |
| Vector Databases (2)        | [YouTube](https://www.youtube.com/watch?v=gl1r1XV0SLw)               |
| AI Notes Video 1            | [YouTube](https://www.youtube.com/watch?v=djGCytw0XZg)               |
| AI Notes Video 2            | [YouTube](https://www.youtube.com/watch?v=JV7Wy6V-tgI)               |
| AI Notes Video 3            | [YouTube](https://www.youtube.com/watch?v=rheqk-L7Yes)               |
| AI Notes Video 4            | [YouTube](https://www.youtube.com/watch?v=6AgndHSkHFI)               |
| AI Notes Video 5            | [YouTube](https://www.youtube.com/watch?v=2lnSx50ssY0)               |


### Articles & Docs


| Topic                        | Link                                                                                         |
| ---------------------------- | -------------------------------------------------------------------------------------------- |
| Eval Skills (OpenAI)         | [developers.openai.com](https://developers.openai.com/blog/eval-skills)                      |
| Ultimate Coding Prompt Guide | [GitHub](https://github.com/VoloBuilds/prompts/blob/main/ultimate-coding-prompt-guide.md)    |
| Claude Code Quickstart       | [code.claude.com](https://code.claude.com/docs/en/quickstart)                                |


### Source Notes

- [[AI notes]]
- [[LLM]]
- [[AI Usages]]
- [[AI Security]]
- [[AI Works]]
- [[AI Content]]
- [[CC]]
- [[Claude Code]]
- [[Claude Code Installation]]
- [[Learning everything using Obsidian, Gemini, and Cursor]]
- [[2026-09-26 - Complete RAG Pipeline Tutorial Build a PDF Agent with Python, LangChain, & Groq]]
- [[Vector Databases]]
- [[Tiktok]]
- [[Tiktok Scripts]]
- [[Random Knowledge]]

---

*Last updated: 2026-10-06*
