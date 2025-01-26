
# Web page Broshure 
The goal of this project is to build a tool that takes a webpage URL and the name of the company as input and provides a useful structure information that can fill a broshure, using an Open-Source model (Llama 3.2) running locally via Ollama.

This project demonstrates:
- Web Scraping, Content Extraction, and Cleaning: The ability to extract a webpage's title, text, json and url using BeautifulSoup, with error handling for failed HTTP requests.
- Ollama Model Integration: Three methods of interacting with the Ollama model running on a local server to summarize the webpage’s content:
    1) Direct HTTP call via requests
    2) Using the Ollama Python package
    3) Connecting via OpenAI API-style calls for flexibility.
- Markdown Formatting: The formatted summarized output is displayed in a clean and readable Markdown format, making it suitable for presentations or reports.
- Error handling on several parts
- One shot prompting example and Chaining (Multi step prompting).

**Model used**
llama3.2

**Benefits:**
1. No API charges - open-source
2. Data doesn't leave your box

**Disadvantages:**
1. Significantly less power than Frontier Model

## Installation of Ollama

Simply visit [ollama.com](https://ollama.com) and install!

Once complete, the ollama server should already be running locally.  
If you visit:  
[http://localhost:11434/](http://localhost:11434/)

You should see the message `Ollama is running`.  

If not, bring up a new Terminal (Mac) or Powershell (Windows) and enter `ollama serve`  
And in another Terminal (Mac) or Powershell (Windows), enter `ollama pull llama3.2`  
Then try [http://localhost:11434/](http://localhost:11434/) again.

To stop the run in another terminal write:
 - ps aux | grep ollama  obtain the PID  for ollama serve
 - kill -9 #####

If Ollama is slow on your machine, try using `llama3.2:1b` as an alternative. Run `ollama pull llama3.2:1b` from a Terminal or Powershell.
