# rag_tutorial
For Harvard GenEd 1188 Generative AI General Education course final project.

This is designed to be a potential section activity for students taking this class next year.

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


## Set Up
1. Open your terminal and type in the following command to create an environment for this project:
```
conda create -p venv python==3.10 -y
```
After the creation, you usually will see something similar to this:
```
conda activate /Users/yourusername/location/to/this/project/rag-tutorial/venv
```
Whenever you start working on this project, remember to activate the environment first by typing the above in the terminal.

You can type
```
conda deactivate
```
to deactivate the environment.

2. Create a `.env` file in this project folder. Store your OpenAI API key in it by typing the following in the `.env` file and assigning your OpenAI API key to this variable:
```
OPENAI_API_KEY=
```

3. Create a `data` directory in this project folder. Put any PDF's as you want in it.

4. Create a `requirements.txt` in this project folder for us to install four important libraries. Put the following in your `requirements.txt`:
```
llama-index
openai
pypdf
python-dotenv
```
These four libraries are the ones we are using for this simple RAG tutorial. 
* [LlamaIndex](https://www.llamaindex.ai/open-source) is a data framework for connecting custom data sources to large language models. 
* [openai](https://platform.openai.com/docs/introduction) is OpenAI's API. The LLM we are using here is from OpenAI. If you prefer some other LLMs, you should update this file accordingly. 
* [pypdf](https://pypi.org/project/pypdf/) is a library which can help us split, merge, crop, and transform the pages of PDF files. It can retrieve text and metadata from PDF's too.
* [python-dotenv](https://pypi.org/project/python-dotenv/) is for loading our API key from the environment file.

To install all the required libraries all at once, simply type the following in your terminal:
```
pip install -r requirements.txt
```
You should update this `requirements.txt` as you develop your project if you end up using some other libraries to do fancy stuff -- this is for other people later if they want to recreate your project!

5. Create a `test.ipynb` jupyter notebook. If you want to run it locally, you might need to install `ipykernel` too:
```
pip install ipykernel
```

## Sources
* [IBM Technology](https://www.youtube.com/watch?v=hH4WkgILUD4)
* [Krish Naik](https://www.youtube.com/watch?v=T-D1OfcDW1M)