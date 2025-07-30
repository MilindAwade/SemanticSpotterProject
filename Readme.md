# Semantic Spotter Project

### Submitted by: Milind Awade 
### Batch - ML-C67

A comprehensive Retrieval-Augmented Generation (RAG) system designed for the insurance domain, leveraging LangChain framework for intelligent document querying.

#### Table of Contents

Project Overview

Technical Approach

System Architecture

Technology Stack

Contact Information

## Project Overview
This project develops a sophisticated generative search system capable of delivering accurate, contextually relevant responses to queries based on insurance policy documentation. The system employs advanced natural language processing techniques to understand complex insurance documents and provide precise answers to user inquiries.
Documentation: Policy documents are available in the ./documents directory.

## Technical Approach
### Framework Selection
The implementation utilizes LangChain, a comprehensive framework designed to streamline Large Language Model (LLM) application development. LangChain provides an extensive ecosystem of tools, components, and interfaces that facilitate the construction of sophisticated LLM-centric applications with seamless integration capabilities across multiple language model providers including OpenAI, Cohere, and Hugging Face.
Core Design Principles
LangChain's architecture emphasizes composition and modularity, enabling rapid development of complex applications through strategic component integration. The framework's language model-agnostic design ensures flexibility and scalability while providing essential abstractions for LLM application development.

### Framework Components

#### Primary Elements:
Modular Components: Abstracted interfaces for language model operations with comprehensive implementation collections
Use-Case Specific Chains: Pre-configured component assemblies optimized for specific applications with customization capabilities

#### Fundamental Building Blocks:

Model I/O: Language model interfaces (LLMs, Chat Models, Prompts, Output Parsers)
Retrieval: Application-specific data management (Document loaders, transformers, embedding models, vector stores, retrievers)
Chains: Sequential LLM call construction for complex workflows
Memory: Application state persistence across chain executions
Agents: Dynamic tool selection based on high-level directives
Callbacks: Logging and streaming capabilities for intermediate chain processes

## System Architecture
### Processing Pipeline

### 1. Document Ingestion and Processing

Implementation: PyPDFDirectoryLoader for efficient PDF batch processing from designated directories

Capability: Automated extraction and standardization of insurance policy documents

### 2. Intelligent Document Segmentation

Method: RecursiveCharacterTextSplitter with hierarchical splitting strategy

Configuration: Parameterized splitting sequence ["\n\n", "\n", " ", ""] to preserve semantic coherence

Objective: Maintain paragraph, sentence, and word integrity for optimal embedding generation

### 3. Vector Embedding Generation

Service: OpenAI Embeddings for high-quality vector representations

Capabilities: Comprehensive support for similarity search, text comparison, and semantic analysis operations

Architecture: Dual-method implementation for document embedding and query embedding

### 4. Vector Storage and Caching

Database: ChromaDB for persistent vector storage with optimized retrieval performance

Enhancement: CacheBackedEmbeddings for improved computational efficiency

### 5. Document Retrieval System

Primary Interface: VectorStoreRetriever for unstructured query processing

Functionality: Document-language model integration with flexible retrieval mechanisms beyond traditional vector store limitations

### 6. Result Re-ranking Enhancement

Technology: HuggingFace Cross Encoder with BAAI/bge-reranker-base model

Purpose: Relevance optimization through query-response pair scoring for improved result accuracy

### 7. Chain Integration and Response Generation

Implementation: LangChain Chains for multi-component integration

Configuration: Custom prompt template (rlm/rag-prompt) from LangChain Hub for RAG-specific optimization

Capability: Complex workflow construction through chain composition and component integration

## System Workflow Visualization
The system architecture follows a structured data flow:

PDF Documents → Processing → Chunking → Embedding → Vector Storage → Query Processing → Retrieval → Re-ranking → Response Generation

Architecture diagrams added to the project report pdf.

Langchain Model I/O and Data Connection Depiction/Flow diagram added to the jupyter notebook code.

### Technology Stack
Python 3.12.7

languageOpenAI 1.93.0

LangChain 0.3.26


### Contact Information
#### Developer: Milind Awade
For technical inquiries, collaboration opportunities, or project-related questions, please feel free to reach out.
