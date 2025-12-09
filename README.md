# Evaluating-Faithfulness-in-Agentic-RAG-Systems-for-e-Governance-applications-LLM-Based

This repository has been established in conjunction with the publication of the research paper titled **Evaluating Faithfulness in Agentic RAG Systems for e-Governance applications using LLM-Based Judging Frameworks** and serves as a supplementary resource for researchers interested in LLM-based Faithfulness evaluation in RAG and Multi-Agent systems. Our example use case is dedicated to E-Government Services.

### Citation
```bibtex
@Article{bdcc9120309,
AUTHOR = {Papageorgiou, George and Sarlis, Vangelis and Maragoudakis, Manolis and Magnisalis, Ioannis and Tjortjis, Christos},
TITLE = {Evaluating Faithfulness in Agentic RAG Systems for e-Governance Applications Using LLM-Based Judging Frameworks},
JOURNAL = {Big Data and Cognitive Computing},
VOLUME = {9},
YEAR = {2025},
NUMBER = {12},
ARTICLE-NUMBER = {309},
URL = {https://www.mdpi.com/2504-2289/9/12/309},
ISSN = {2504-2289},
ABSTRACT = {As Large Language Models (LLMs) are core components in Retrieval-Augmented Generation (RAG) systems for knowledge-intensive tasks, concerns regarding hallucinations, redundancy, and unverifiable outputs have intensified, particularly in high-stakes domains, such as e-government. This study proposes a modular, multi-pipeline framework for statement-level faithfulness evaluation for characterizing hallucination and redundancy across both simple and agentic RAG pipelines. Using GPT-4.1, Claude Sonnet-4.0, and Gemini 2.5 Pro as LLM-based judges, this study examines how tool-specific attribution within agentic multi-tool architectures influences the interpretability and traceability of the generated content. By using a modular agentic RAG framework combining symbolic (GraphRAG), semantic (embedding), and real-time (web) retrieval, we benchmark hallucination and redundancy patterns, using state-of-the-art LLM judges. The study examines RAG and agent-based pipelines that attribute outputs to distinct tools, in contrast to traditional single-source RAG systems that rely on aggregated retrieval. Using e-government data sourced from the European Commission’s Press Corner, our evaluation framework assesses not only the frequency, but also the source-aware detectability of hallucinated content. The findings provide actionable insights into how source granularity and retrieval orchestration impact faithfulness evaluation across different pipeline architectures, while also suggesting new directions for explainability-aware RAG design. The study contributes a reproducible, modular framework for automated faithfulness assessment, with implications for transparency, governance compliance, and trustworthy AI deployment.},
DOI = {10.3390/bdcc9120309}
}
```

## Introduction

The repository contains a Jupyter notebook designed to run in Google Colab. It is built using the robust open-source [Haystack](https://github.com/deepset-ai/haystack) framework, which provides an end-to-end solution for Large Language Models (LLMs).

It offers an LLM-based Faithfulness evaluation pre-configured with GPT/ Claude/ Gemini, allowing for different modes of RAG evaluation with embeddings, graphs, web search, and Agentic. Users can index their data in their Neo4J database, engage in interactive conversations with the Gen AI models of their choice, and assess the faithfulness of their pipelines using the custom-made LLM-based evaluators based on extracted statements.

The application is based on prior research that can be found in [Hybrid Multi-Agent GraphRAG for E-Government: Toward a Trustworthy AI Assistant](https://www.mdpi.com/2076-3417/15/11/6315), with the RAG architecture as a basis, allowing modular selection of models and components.
```bibtex
@Article{app15116315,
AUTHOR = {Papageorgiou, George and Sarlis, Vangelis and Maragoudakis, Manolis and Tjortjis, Christos},
TITLE = {Hybrid Multi-Agent GraphRAG for E-Government: Towards a Trustworthy AI Assistant},
JOURNAL = {Applied Sciences},
VOLUME = {15},
YEAR = {2025},
NUMBER = {11},
ARTICLE-NUMBER = {6315},
URL = {https://www.mdpi.com/2076-3417/15/11/6315},
ISSN = {2076-3417},
ABSTRACT = {As public institutions increasingly adopt AI-driven virtual assistants to support transparency and citizen engagement, the need for explainable, accurate, and context-aware language systems becomes vital. While traditional retrieval-augmented generation (RAG) frameworks effectively integrate external knowledge into Large Language Models (LLMs), their reliance on flat, unstructured document retrieval limits multi-hop reasoning and interpretability, especially with complex, structured e-government datasets. This study introduces a modular, extensible, multi-agent graph retrieval-augmented generation (GraphRAG) framework designed to enhance policy-focused question answering. This research aims to provide an overview of hybrid multi-agent GraphRAG architecture designed for operational deployment in e-government settings to support explainable AI systems. The study focuses on how the hybrid integration of standard RAG, embedding-based retrieval, real-time web search, and LLM-generated structured Graphs can optimize knowledge discovery from public e-government data, thereby reinforcing factual grounding, reducing hallucinations, and enhancing the quality of complex responses. To validate the proposed approach, we implement and evaluate the framework using the European Commission’s Press Corner as a data source, constructing graph-based knowledge representations and embeddings, and incorporating web search. This work establishes a reproducible blueprint for deploying AI systems in e-government that require structured reasoning in comprehensive and factually accurate question answering.},
DOI = {10.3390/app15116315}
}
```

## Example Use Case

The use case presented in our research focuses on enhancing E-Government Services through a state-of-the-art, modular, and reproducible Multi-Agent architecture utilizing, Embeddings, Graphs, Web Search and LLMs for QA and statements generation and extraction.

In our example, we use publicly available sources, such as the [Press Corner](https://ec.europa.eu/commission/presscorner) and Web Search. The Press Corner data used complies with the terms of use policy, and all appropriate credit goes to the Press Corner. Please note that this repository is not affiliated with, sponsored by, or endorsed by the Press Corner.

Our approach emphasizes evaluation, modularity and reproducibility, with all pipelines, custom components, and setups designed to be flexible and customizable. Users can apply different AI models, utilize their databases, integrate web search tools, implement various preprocessing steps, deploy and evaluate agents, and define their data sources.


## Access Instructions

To access the notebook in Google Colab, click the badge below and follow the guidelines:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gpapageorgiouedu/Evaluating-Faithfulness-in-Agentic-RAG-Systems-for-e-Governance-applications-LLM-Based/blob/main/Faithfulness_eval_with_LLMs.ipynb)

Example LLM-based faithfulness evaluation with indexing and querying pipelines is set up as demonstrated in our research. For usage, you will need to create your own index. All components are modular and scalable, allowing graph setups, embeddings index, generative AI models, custom retrievals, prompts, custom statements extractor and evaluators, and other elements to be modified as per users' preferences.


## Features

- **Processing Modes**: Flexible configuration of models and pipelines to control how queries are interpreted and answered.
- **Embeddings Pipeline**: Answer generation powered by embeddings-based retrieval.
- **Graphs Pipeline**: Generates triples from raw text for indexing and supports graph-based answering through custom components.
- **Graph and Embeddings Indexing**: Dual indexing options enabling efficient retrieval and grounded answer generation.
- **Web Search Pipeline**: Augments answers with external search results to provide comprehensive, context-rich responses.
- **Agentic Workflows**: Multi-agent reasoning that leverages the tools of the standard pipelines, with a custom dedicated faithfulness evaluation component.
- **Faithfulness Evaluation**: LLM-based evaluation ensuring generated answers are directly grounded in the provided content, preconfigured to run with different models such as GPT, Claude, and Gemini.
- **Triples Audit**: Evaluation of LLM-generated triples, verifying their grounding and relevance within indexed knowledge.



## Repository Contents

This repository contains the following structure:

- **`Faithfulness_eval_with_LLMs.ipynb`**: The Jupyter Notebook usable from Google Colab that contains the main code and demonstrations for using the application with documentation.


## Compliance with AI EU Act

This project as an extension to prior research is designed with compliance in mind regarding the [European Union's AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai), [European Union's AI Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32024R1689), both for current use and for future updates as the regulatory landscape evolves. Users who deploy, modify, or extend this application should be aware of the AI EU Act's guidelines and ensure compliance with applicable regulations.

