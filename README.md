# rag_tutorial
For Harvard GenEd 1188 Generative AI General Education course final project

## What is Retrieval-Augmented Generation (RAG)?

* RAG is a framework that improves the accuracy and timeliness of large language models (LLMs) by incorporating external, current data.

### LLM Challenges
1. Lack of sources.
2. Quickly outdated information.

### Concept of "Retrieval-Augmented"
* RAG adds to an LLM's fixed knowledge by incorporating a content store that can be as broad as the Internet.
* The method starts with retrieving relevant information, which is then combined with the user's query to generate a response.

### Structure of a "New" Prompt
* After adding retrieval-augmentation, the prompt includes three parts:
  * The main instruction.
  * The retrieved content.
  * The user's question.

## Benefits of RAG
* **Updating information:** Updates to the data repository keep the model current without needing retraining.
* **Source verification:** The model uses primary source data to inform its responses, providing evidence for its answers.
* **Minimizing errors:** Relying less on pre-trained data reduces errors and the creation of false information.
* **Acknowledging limits:** If the data does not support a reliable answer, the model can say "I don't know" instead of providing a potentially misleading response.
