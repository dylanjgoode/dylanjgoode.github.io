---
title: "El Palabrero"
excerpt: "A personal project exploring AI-driven language learning tools."
collection: portfolio
order: 3
---

**[El Palabrero](https://github.com/dylanjgoode/El_Palabrero)**

Palabrero is a Streamlit app that helps you practice Spanish conversation and tracks your progress with GPT‑powered analytics and vocabulary insights.

![Palabrero](/images/audiofeature.png)

### Features

- **Chat tutor**:  
  - Chat in Spanish with an AI tutor guided by a custom `system_prompt.md`.  
  - Per-message analysis (tense, error types, topics, notable vocabulary) when GPT is available.

- **Roleplay scenarios**:  
  - Practice Spanish in specific contexts (e.g., "Café in Madrid", "Job Interview").  
  - Create, edit, and manage custom scenarios from the sidebar.  
  - The AI adapts its persona while maintaining correction behavior.

- **Learning analytics dashboard**:  
  - **Tense usage** over time.  
  - **Error types** distribution (grammar, conjugation, vocabulary, etc.).  
  - **Topics** you speak about the most.  
  - **Vocabulary growth** and “new words per conversation”.  
  - Conversation summaries and message-level detail.


- **Mochi flashcards generator**:  
  - Generate flashcards from your mistakes in selected conversations.  
  - Review and delete individual cards before downloading.  
  - Export as `.mochi` files for import into [Mochi](https://mochi.cards/).
