
# HuggingFace Pipelines
The Hugging Face transformers library is an incredibly versatile and powerful tool for natural language processing (NLP).This project demonstrates how to leverage Hugging Face in inference mode, using various tasks such as Sentiment Analysis, Text Classification, Named Entity Recognition (NER), Text Generation, Question Answering with Context, and Summarization with open-source models running locally. But you can also use Hugging Face Inference Server (from huggingface_hub import InferenceApi), available at a cost, it allows you to run these models in a cloud environment on Hugging Face's infrastructure, meaning the computation is done remotely on those servers, not on your local machine.


This project demonstrates:
- Inference using open-source models through the high-level API known as Pipelines.
- Application of models based on the transformer architecture.
- Secure handling of sensitive information using environment variables (.env), a common practice in local development. This prevents sensitive data, such as API tokens or database credentials, from being committed to version control (e.g., Git). To enhance security, the .env file is often added to .gitignore to avoid accidental exposure. 
- Error handling for missing or incorrectly set tokens, ensuring smooth operation.
- Suppress warnings from Hugging Face transformers library

**Model used**
The models are configured with default settings in most cases, but users have the flexibility to select and customize their choice of model. The following models were applied for specific this specific tasks:
-  Text Classification/ Sentiment Analysis: distilbert-base-uncased-finetuned-sst-2-english : This model is a fine-tune checkpoint of DistilBERT-base-uncased.
- NER: bert-large-cased-finetuned-conll03-english
- QA with Context: distilbert-base-cased-distilled-squad 
- Summarization: distilbart-cnn-12-6 
- Traslation to french: t5-base  and spanish:  Helsinki-NLP/opus-mt-en-es
- Classification with labels: bart-large-mnli
- Text Generation: gpt2, this is the smallest version of GPT-2, with 124M parameters.


**Benefits:**
1. No API charges - open-source
ollama vs hgging =face
2. Data doesn't leave your box 

**Disadvantages:**
1. Significantly less power than Frontier Model

## Setting up HuggingFace
To get started, you’ll need to create an account on [Hugging Face](https://huggingface.co). Once registered, navigate to the Settings section from the user menu located at the top right corner of the page. From there, generate a new API token with both read and write permissions. This access token allows you to interact with Hugging Face models both locally on your computer and in the cloud (e.g., Google Colab).

For further documentation on Hugging Face Pipelines, you can explore the available tasks on the Transformers pipeline page https://huggingface.co/docs/transformers/main_classes/pipelines. You will find a comprehensive list of tasks under the "Tasks" section. Scroll down and expand the parameters to see the available options for each task. 
