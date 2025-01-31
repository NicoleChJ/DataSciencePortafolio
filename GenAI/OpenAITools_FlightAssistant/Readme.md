
# Flight Assistant with Gradio
This project implements an interactive chatbot powered by OpenAI's GPT-4o-mini, DALL·E 3, and TTS-1 with Onyx voice. Initially, the chatbot functions as a general assistant, responding to user queries. In the second phase, it is enhanced with tools that allow it to fetch real-time flight prices, a feature it previously lacked. The third phase transforms the assistant into a multimodal experience, where it not only displays text but also plays audio responses and shows relevant images if specific cities are mentioned in the conversation.

This project demonstrates:
- OpenAI Model Integration,leveraging OpenAI’s cloud-based AI model for real-time responses.
- Use of tools, so extends functionality by allowing the LLM to call external functions, such as retrieving flight prices.
- Load environment variables.
- Creating an engaging multimodal experience by adding audio and image output.
- Send the history message in OpenAI format: Gradio already setup for us: 

[
    {"role": "system", "content": "system message here"},
    {"role": "user", "content": "first user prompt here"},
    {"role": "assistant", "content": "the assistant's response"},
    {"role": "user", "content": "the new user prompt"},
]

- Use Gradio as a chat interface with support for light and dark modes. Deploy it locally or generate a public URL, which remains valid for 72 hours. For free permanent hosting and GPU upgrades, run gradio deploy from the terminal in the working directory to deploy the application to Hugging Face Spaces.


![Chatbot Preview](gradioUI.png)

With tool

![Chatbot Preview2](gradioUITools.png)

As multimodal

![Chatbot Preview3](multimodal.png)

**Model used**
gpt-4o-mini,  dall-e-3 and tts-1 with onyx voice.

**Benefits:**
1. The higest power the market offers as is a Frontier LLM model

**Disadvantages:**
1. API charges
2. Data leaves your box

## Audio Setup
For Mac users: Open a new command prompt and run this to make sure it's installed OK
`ffmpeg -version`, if not:

1. Install homebrew if you don't have it already by running this in a Terminal window and following any instructions:  
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

2. Then install FFmpeg with `brew install ffmpeg`

3. Verify your installation with `ffmpeg -version` and if everything is good, within Jupyter Lab do Kernel -> Restart kernel to pick up the changes

4. If did not work manually  one quick solution is to set the PATH in your script: 
import os
os.environ['PATH'] = '/opt/homebrew/bin:' + os.environ['PATH']


## OpenAI Setup

1. Create an OpenAI account if you don't have one by visiting:
https://platform.openai.com/

2. OpenAI asks for a minimum credit to use the API. 

You can add your credit balance to OpenAI at Settings > Billing:  the minimun amounth for my country is $5
https://platform.openai.com/settings/organization/billing/overview

I recommend you disable the automatic recharge!

3. Create your API key

The webpage where you set up your OpenAI key is at https://platform.openai.com/api-keys - press the green 'Create new secret key' button and press 'Create secret key'. Keep a record of the API key somewhere private; you won't be able to retrieve it from the OpenAI screens in the future. It should start `sk-proj-`.

Other frontier models at:
- Claude API at https://console.anthropic.com/ from Anthropic
- Gemini API at https://ai.google.dev/gemini-api from Google


4. When you have these keys, please create a new file called `.env` in your project root directory. The filename needs to be exactly the four characters ".env" rather than "my-keys.env" or ".env.txt". Here's how to do it:
Type OPENAI_API_KEY=xxxx


