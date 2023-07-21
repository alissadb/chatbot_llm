# Chatbot

Bot 🤖 = Streamlit 👑 + Langchain 🦜️⛓️ + LLaMA 🦙

1. **Streamlit:**
   The app is built using [Streamlit](https://streamlit.io/) and allows you to interact with a language model-based chatbot. The app enables you to have conversations with the chatbot and see its responses.

2. **Langchain:**
   [Langchain](https://python.langchain.com/docs/get_started/introduction.html) is a Python library for natural language processing tasks. It provides various functionalities, including text preprocessing, language detection, sentiment analysis, and more. The chatbot app utilizes Langchain's capabilities to process and understand user input.

3. **LLaMA:**
   [LLaMA](https://ai.meta.com/blog/large-language-model-llama-meta-ai/) is a pre-trained language model capable of generating creative and contextually relevant responses in conversations. It powers the chatbot's language generation and understanding abilities.

![Example](figures/Example.png)

## Installation

1. Make sure you have [Python](https://www.python.org/) and [Poetry](https://python-poetry.org/) installed on your system.
2. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/alissadb/chatbot.git
   ```

3. Navigate to the repository directory:

   ```bash
   cd chatbot
   ```

4. Install Task on your system by following the instructions in the [Task documentation](https://taskfile.dev/#/installation). The repository uses Task to define and run tasks in a simple and declarative way.

5. To set up the local development environment with the required dependencies. Install the local environment:

   ```bash
   task setup-local-env
   ```

## Usage

### Running the 🤖

1. Download a model, for example `Llama-2-7B-Chat-ggml` from Hugging Face ([link](https://huggingface.co/localmodels/Llama-2-7B-Chat-ggml/blob/main/llama-2-7b-chat.ggmlv3.q2_K.bin)) and save it under the `models/` directory.

2. Change the model name in `app.py` in this line

```python
llm_chain = get_llm_chain(model_name="models/llama-2-7b-chat.ggmlv3.q2_K.bin")
```

2. To run the 🤖 run the following command:

```bash
task run-app
```

The app will be accessible at `http://localhost:8501` in your web browser.
