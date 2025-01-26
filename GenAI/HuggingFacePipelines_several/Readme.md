
# Hugging Face Pipelines
The Hugging Face diffusers library is an incredibly versatile and powerful.This project demonstrates how to leverage Hugging Face in inference mode, using various tasks such as audio and image generation with open-source models running locally. But you can also use Hugging Face Inference Server (from huggingface_hub import InferenceApi), available at a cost, it allows you to run these models in a cloud environment on Hugging Face's infrastructure, meaning the computation is done remotely on those servers, not on your local machine.


This project demonstrates:
- Inference using open-source models through the high-level API known as Pipelines.
- Application of models based on the diffusers architecture.
- Secure handling of sensitive information using environment variables (.env), a common practice in local development. This prevents sensitive data, such as API tokens or database credentials, from being committed to version control (e.g., Git). To enhance security, the .env file is often added to .gitignore to avoid accidental exposure. 
- Error handling for missing or incorrectly set tokens, ensuring smooth operation.
- Suppress warnings from Hugging Face diffusers library.
- Load datasets from Hugging Face.

**Model used**
The models are configured with default settings in most cases, but users have the flexibility to select and customize their choice of model. The following models were applied for specific this specific tasks:
- Image Generation: stabilityai/stable-diffusion-2
- Audio Generation: microsoft/speecht5_tts


**Benefits:**
1. No API charges - open-source
2. Vast Model Repository.
3. Data doesn't leave your box 

**Disadvantages:**
1. Significantly less power than Frontier Model

## Setting up Hugging Face
To get started, you’ll need to create an account on [Hugging Face](https://huggingface.co). Once registered, navigate to the Settings section from the user menu located at the top right corner of the page. From there, generate a new API token with both read and write permissions. This access token allows you to interact with Hugging Face models both locally on your computer and in the cloud (e.g., Google Colab).

For further documentation on Hugging Face Pipelines, you can explore the available tasks on the diffusers pipeline page https://huggingface.co/docs/diffusers/en/api/pipelines/overview. 
