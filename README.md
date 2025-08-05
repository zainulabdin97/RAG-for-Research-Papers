# AI Research Assistant with RAG 🧠

## Project Overview

This project demonstrates a **Retrieval-Augmented Generation (RAG)** system designed to combat the common problem of LLM hallucination on specialized data. It provides a reliable Q&A tool for technical research papers, ensuring all generated responses are grounded in the provided source documents.

---

## The Problem

In fields with rapidly-evolving research, relying on a standard LLM to answer questions about brand-new papers can lead to several challenges:

* Information Overload: Manually sifting through dense papers is time-consuming.
* LLM Hallucination: LLMs may generate fabricated information when they lack specific knowledge.
* Lack of Verifiable Sources: It's impossible to verify the accuracy of the LLM's claims.

---

## The Solution: A RAG System

This project builds a full-stack RAG pipeline. The system processes a collection of research papers, creating a searchable knowledge base. When a user asks a question, it intelligently retrieves the most relevant information and uses it to augment a Gemini model's response. The final output includes a concise answer and the exact source snippets.

---

## Key Features

* **Robust Data Ingestion:** Reads and processes multiple PDF research papers.
* **Advanced Text Cleaning:** A cleaning pipeline removes artifacts from PDF extraction.
* **Efficient Vectorization:** Converts text into high-quality embeddings.
* **Lightning-Fast Search:** Utilizes a **FAISS** index for rapid semantic search.
* **Intelligent Generation:** Employs the **Gemini model** to synthesize accurate and context-aware answers.

---

### **Demonstration**

Here is an example of the system in action, answering a question and citing its sources:

#### **User Query**
> What is a Long term memory?

#### **AI Assistant's Answer**
Some researchers view conversational memory mechanisms as a form of self-evolution for large language models (LLMs). Early methods involved concatenating full dialogue histories into prompts to preserve context, but these were limited by the model's context window and unsuitable for long-term interactions.

More efficient memory systems developed to address this include:

ReadAgent (Lee et al. 2024): Summarizes long texts for on-demand retrieval, improving context utilization.
Memory Bank (Zhong et al. 2024): Uses vector-based similarity search to enhance storage and access, though scalability remains an issue.
A MEM (Xu et al. 2025): Constructs an evolving knowledge graph, improving organization at the cost of structural complexity.
These methods enhance user alignment through few-shot prompts that combine past interactions with current inputs. However, they operate externally and do not improve the LLM's internal cognition, which remains fixed and non-evolving. "Memory focused baselines" are also used in evaluations on long-term dialogue tasks.

---
