---
layout: default
title: Projects
description: "Data science and machine learning projects by Dallin Nielson."
---

<div class="page-header">
  <div class="page-header-inner">
    <h1>Projects</h1>
    <p>Applied machine learning, NLP, and data engineering — built around real workflows.</p>
  </div>
</div>


<section class="page-section">

  <!-- KNOWLEDGE MANAGEMENT & SUPPORT OPERATIONS -->
  <h2 class="section-heading" id="knowledge-management">Knowledge Management & Support Operations</h2>
  <p style="color: var(--text-secondary); margin-bottom: 2rem;">
    These projects sit at the core of my work. Each one applies machine learning or AI to a specific, well-understood problem in knowledge and support operations — built around the KCS methodology and designed to help real people do their jobs better.
  </p>

  <div class="projects-list">

    <!-- PROJECT 1 -->
    <a class="project-card" href="https://github.com/Daly-Llama/link_validator" target="_blank" rel="noopener">
      <div class="project-card-header">
        <h3>KCS Link Validator</h3>
        <span class="project-label">NLP · Classification · Embeddings</span>
      </div>
      <p>
        A complete end-to-end ML pipeline that predicts whether a help desk analyst linked the correct knowledge article to a support ticket. Built for Knowledge-Centered Service (KCS) environments, the system scrapes and parses a live knowledge base, generates synthetic incidents using OpenAI with randomized situational modifiers, embeds both articles and incidents using SentenceTransformers, and trains a Logistic Regression classifier on cosine similarity and metadata features. Achieves 90% accuracy and 0.95 ROC-AUC with full SHAP explainability.
      </p>
    </a>

    <!-- PROJECT 2 -->
    <a class="project-card" href="https://github.com/Daly-Llama/semantic_search" target="_blank" rel="noopener">
      <div class="project-card-header">
        <h3>KCS Semantic Search</h3>
        <span class="project-label">NLP · Semantic Search · Information Retrieval</span>
      </div>
      <p>
        A semantic search engine that surfaces the most relevant knowledge articles for a support incident using sentence embeddings and cosine similarity. Built specifically for KCS environments, the model embeds only the Issue and Environment fields of each article — the customer-facing language KCS is designed to produce — and includes an explanation layer that surfaces shared keywords, named entities, and the strongest sentence-level matches so analysts understand why each result was recommended. Achieves 0.94 MRR and 99.8% Recall@10 on synthetic data.
      </p>
    </a>

    <!-- PROJECT 3 -->
    <a class="project-card" href="https://github.com/Daly-Llama/kcs_chatbot" target="_blank" rel="noopener">
      <div class="project-card-header">
        <h3>KCS RAG Support Chatbot</h3>
        <span class="project-label">RAG · LLM · Conversational AI</span>
      </div>
      <p>
        A retrieval-augmented generation chatbot that answers support questions grounded in a KCS knowledge base, built with LangChain, Chroma, and a fine-tuned GPT-4o Mini model trained on KCS response behavior. The pipeline retrieves the most relevant article chunks for each query, rewrites follow-up questions into standalone form to preserve conversation context, and enforces strict grounding rules so the model never answers beyond what the knowledge base contains. Deployed as an interactive Streamlit application.
      </p>
    </a>

    <!-- PROJECT 4 -->
    <a class="project-card" href="https://github.com/Daly-Llama/ticket_classifier" target="_blank" rel="noopener">
      <div class="project-card-header">
        <h3>Support Ticket Classification</h3>
        <span class="project-label">NLP · Text Classification · TF-IDF</span>
      </div>
      <p>
        An NLP pipeline that applies TF-IDF vectorization and multi-class classification to predict the topic category of customer support tickets from their text descriptions. The project compared Logistic Regression, Decision Trees, and Multinomial Naive Bayes via GridSearchCV across progressively refined problem formulations — from 16-class classification down to binary — diagnosing class imbalance and data quality issues at each stage. The final binary classifier achieved 79% accuracy predicting hardware issue tickets, with the multi-class challenge documented as a foundation for future work.
      </p>
    </a>
  </div>


  <hr>


  <!-- OTHER PROJECTS -->
  <h2 class="section-heading" id="other-projects">Other Projects</h2>

  <div class="projects-grid" style="margin-top: 2rem;">

    <!-- PROJECT 5 -->
    <a class="project-card" href="https://github.com/Daly-Llama/fraud_detection" target="_blank" rel="noopener">
      <h3>Credit Card Fraud Detection</h3>
      <span class="project-label" style="text-align: left ">Classification · Decision Trees</span>
      <p>
        A Decision Tree classifier that predicts fraudulent credit card transactions across 1 million records, designed with regulatory transparency as an explicit requirement alongside accuracy. The model achieves 100% recall on fraud cases in the test set — missing only 2 of 26,131 fraudulent transactions — while remaining fully interpretable: every decision can be traced through the tree and explained to auditors. Includes cross-validation and a documented deployment recommendation that prioritizes analyst oversight over automated blocking.
      </p>
    </a>

    <!-- PROJECT 6 -->
    <a class="project-card" href="https://github.com/Daly-Llama/session_tunes" target="_blank" rel="noopener">
      <h3>Traditional Irish Tune Popularity Analysis</h3>
      <span class="project-label" style="text-align: left ">Web Scraping · EDA</span>
      <p>
        An end-to-end data project that scrapes, parses, and cleans unstructured session data from a live traditional Irish music community site, then applies exploratory analysis to surface patterns in tune popularity, regional variation, and session frequency. Demonstrates the full pipeline from raw web data to structured insight.
      </p>
    </a>

  </div>

</section>