# Week 7: Retrieval-Augmented Generation (RAG) using Custom Documents

## Project Overview

This project demonstrates the implementation of a simple Retrieval-Augmented Generation (RAG) system capable of answering user questions using information extracted from a custom document.

The system combines semantic search and text generation by retrieving relevant document sections and using them as context for generating grounded responses. Unlike traditional language models that rely only on pre-trained knowledge, RAG enhances answer quality by incorporating external document-based information during inference.

The custom document used in this project is:

**Internet of Things: A Survey on Enabling Technologies, Protocols, and Applications**

---

## Objectives

* Build a simple Retrieval-Augmented Generation (RAG) pipeline.
* Extract and process text from a custom PDF document.
* Divide the document into smaller chunks for efficient retrieval.
* Generate semantic embeddings using Sentence Transformers.
* Store embeddings in a FAISS vector database.
* Retrieve relevant document chunks based on user queries.
* Generate context-aware answers using a language model.
* Evaluate retrieval effectiveness and answer quality.
* Analyze the impact of retrieval depth (Top-K) on system performance.

---

## Document Used

**Title:** Internet of Things: A Survey on Enabling Technologies, Protocols, and Applications

The document provides detailed information about:

* Internet of Things (IoT)
* IoT Architecture
* Communication Protocols
* MQTT
* CoAP
* AMQP
* Smart Applications
* IoT Challenges
* Enabling Technologies

---

## Methodology

### 1. Document Processing

* Load the PDF document.
* Extract textual content from all pages.
* Merge extracted text into a single corpus.

### 2. Text Chunking

* Split the document into smaller chunks.
* Chunk size set to 500 characters.
* Enables efficient retrieval and embedding generation.

### 3. Embedding Generation

* Use SentenceTransformer (`all-MiniLM-L6-v2`) to create dense vector embeddings.
* Convert each text chunk into a semantic representation.

### 4. Vector Database Creation

* Store embeddings using FAISS.
* Perform similarity search to retrieve relevant information.

### 5. Retrieval Mechanism

* Convert user queries into embeddings.
* Search the FAISS index for the most relevant document chunks.
* Retrieve Top-K relevant contexts.

### 6. Answer Generation

* Combine retrieved context with user queries.
* Use DistilGPT2 for text generation.
* Generate document-grounded answers.

---

## Experimental Setup

### Embedding Model

* SentenceTransformer
* Model: `all-MiniLM-L6-v2`

### Vector Store

* FAISS (Facebook AI Similarity Search)

### Generator Model

* DistilGPT2

### Retrieval Parameter

* Top-K Retrieval = 3

---

## Sample Questions

The RAG system was tested using domain-specific questions:

1. What is Internet of Things?
2. What is MQTT protocol?
3. What are the layers of IoT architecture?
4. What is CoAP?
5. What are the applications of IoT?

---

## Evaluation

### Retrieval Validation

Retrieved document chunks were inspected before answer generation to verify that relevant information was successfully identified.

### Answer Validation

Generated answers were compared with the retrieved context to ensure that responses were grounded in document content.

### Top-K Retrieval Experiment

Different retrieval depths were evaluated:

| Top-K | Observation                                                           |
| ----- | --------------------------------------------------------------------- |
| 1     | Highly focused retrieval but limited context                          |
| 3     | Balanced retrieval with relevant supporting information               |
| 5     | More context available but increased chance of irrelevant information |

Based on experimental observations, **Top-K = 3** provided the best balance between relevance and contextual completeness.

---

## Key Observations

* Semantic embeddings effectively captured document meaning.
* FAISS enabled fast and accurate retrieval of relevant information.
* Retrieved context improved answer grounding compared to standalone text generation.
* The quality of generated answers depended heavily on retrieval quality.
* Top-K retrieval significantly influenced response relevance and completeness.
* Displaying retrieved chunks helped validate the correctness of the retrieval process.

---

## Challenges

* Large PDF documents require efficient chunking strategies.
* Retrieval quality depends on chunk size selection.
* Small language models may generate incomplete or repetitive answers.
* Irrelevant retrieval results can negatively impact generated responses.
* Balancing retrieval depth and answer precision is an important design consideration.

---

## Limitations

* The system was tested on a single research document.
* DistilGPT2 has limited reasoning and generation capabilities compared to larger language models.
* Retrieval effectiveness depends on embedding quality.
* Answers are constrained by the information available within the uploaded document.
* More advanced RAG systems can benefit from larger LLMs and improved vector databases.

---

## Conclusion

A Retrieval-Augmented Generation (RAG) system was successfully developed using a custom IoT research paper. The system integrated document retrieval through FAISS and semantic embeddings with language model-based answer generation.

Experimental results demonstrated that retrieving relevant context before generation improves answer quality and grounding. The project highlights the practical application of RAG systems for question answering over custom documents and provides a foundation for more advanced knowledge retrieval systems.

---

## Technologies Used

* Python
* PyPDF2
* NumPy
* Sentence Transformers
* FAISS
* Hugging Face Transformers
* DistilGPT2

