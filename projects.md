---
layout: default
title: Projects
description: "Data science and machine learning projects by Dallin Nielson."
---

<!-- ============================================================
     PROJECTS PAGE (projects.md)
     WHAT TO EDIT HERE:
       • Each .project-card block — title, description, label, links
       • The .project-label text (category shown in amber above the title)
       • Add/remove entire <div class="project-card"> blocks for more projects
     HOW TO ADD A PROJECT:
       Copy one entire project-card block, paste it in the grid,
       and update the text and links.
     ============================================================ -->

<div class="page-header">
  <div class="page-header-inner">
    <h1>Projects</h1>
    <p>Applied machine learning, NLP, and data engineering — built around real workflows.</p>
  </div>
</div>


<section class="page-section">

  <div class="projects-grid">

    <!-- PROJECT 1 -->
    <div class="project-card">
      <p class="project-label">NLP · Classification · RAG</p>
      <h3>KCS Link Validator</h3>
      <p>
        A complete end-to-end ML pipeline that predicts whether a help desk analyst
        linked the correct knowledge article to a support ticket. Built for
        Knowledge-Centered Service environments, the system scrapes and parses a
        live knowledge base, generates synthetic incidents using OpenAI with
        randomized situational modifiers, embeds both articles and incidents using
        SentenceTransformers, and trains a Logistic Regression classifier on
        cosine similarity and metadata features. Achieves 90% accuracy and
        0.95 ROC-AUC with full SHAP explainability.
      </p>
      <div class="project-links">
        <a href="https://github.com/Daly-Llama/link_validator" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>

    <!-- PROJECT 2 -->
    <div class="project-card">
      <p class="project-label">NLP · Semantic Search · Information Retrieval</p>
      <h3>Semantic KCS Knowledge Search</h3>
      <p>
        A semantic search engine that surfaces the most relevant knowledge articles
        for a support incident using sentence embeddings and cosine similarity.
        Built specifically for KCS environments, the model embeds only the Issue
        and Environment fields of each article — the customer-facing language KCS
        is designed to produce — and includes an explanation layer that surfaces
        shared keywords, named entities, and the strongest sentence-level matches
        so analysts understand why each result was recommended. Achieves 0.94 MRR
        and 99.8% Recall@10 on synthetic data.
      </p>
      <div class="project-links">
        <a href="https://github.com/Daly-Llama/semantic_search" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>

    <!-- PROJECT 3 -->
    <div class="project-card">
      <p class="project-label">RAG · LLM · Conversational AI</p>
      <h3>KCS RAG Support Chatbot</h3>
      <p>
        A retrieval-augmented generation chatbot that answers support questions
        grounded in a KCS knowledge base, built with LangChain, Chroma, and a
        fine-tuned GPT-4o Mini model trained on KCS response behavior. The
        pipeline retrieves the most relevant article chunks for each query,
        rewrites follow-up questions into standalone form to preserve conversation
        context, and enforces strict grounding rules so the model never answers
        beyond what the knowledge base contains. Deployed as an interactive
        Streamlit application.
      </p>
      <div class="project-links">
        <a href="https://github.com/Daly-Llama/kcs_chatbot" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>

    <!-- PROJECT 4 — TEMPLATE: Duplicate this block to add more projects -->
    <!--
    <div class="project-card">
      <p class="project-label">Your Category Here</p>
      <h3>Your Project Title</h3>
      <p>
        Describe what you built, what problem it solves, and what
        tools or methods you used. 2–3 sentences is ideal.
      </p>
      <div class="project-links">
        <a href="https://github.com/yourusername/your-repo" target="_blank" rel="noopener">GitHub</a>
        <a href="#">Write-up</a>
      </div>
    </div>
    -->

  </div>

</section>