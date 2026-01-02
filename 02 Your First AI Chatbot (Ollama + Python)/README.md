# Your First AI Chatbot (Ollama + Python)

A lightweight, terminal-based AI chatbot built with **Python** and **Ollama**, designed to demonstrate how to interact with a local large language model using a minimal and clear code structure.

This project serves as an introductory example for running **local LLMs** and building simple conversational interfaces without external APIs.


## Features

* Runs fully **offline** using local Ollama models
* Simple interactive command-line interface
* Stateless chatbot (no conversation memory)
* Clear and minimal Python implementation
* Easily configurable model selection


## Requirements

* **Python 3.13+**
* **Ollama** installed and running
* At least one Ollama model pulled (default: `qwen3:0.6b`)

To install the model:

```bash
ollama pull qwen3:0.6b
```


## Installation & Usage

### 1. Start the Ollama Server

Open a terminal and run:

```bash
ollama serve
```

Keep this process running in the background.


### 2. Run the Chatbot

Open a new terminal and navigate to the project directory:

```text
02 Your First AI Chatbot (Ollama + Python)
```

Then execute:

```bash
python src/bot.py
```


## How It Works

* User input is sent to the Ollama chat API
* A system prompt enforces:

  * Plain-text output only
  * Very short responses (1–2 sentences)
* The model generates a response, which is printed directly to the terminal
* Typing `q` or `Q` exits the chat loop


## Example Session

```text
Welcome to your personal AI chatbot.
This bot has no memory. Feel free to ask any question.
Enter 'Q' or 'q' to exit the chat.

You: Why is the sky blue?
Robot: The sky appears blue because blue light is scattered more efficiently by the Earth's atmosphere compared to red or orange light. This scattering effect causes the visible light to be predominantly blue, making the sky appear blue.

You: q
Robot: Goodbye, see you later.
```


## Project Structure

```text
.
├── src/
│   └── bot.py        # Chatbot implementation
└── README.md         # Project documentation
```


## Configuration

The model name can be changed directly in `bot.py`:

```python
model_name: str = "qwen3:0.6b"
```

Replace it with any other locally available Ollama model.


## Intended Audience

This project is ideal for:

* Beginners learning how to use Ollama with Python
* Developers experimenting with local LLMs
* Educational demos and tutorials
* Prototyping simple AI assistants


## License

This project is provided for educational and experimental purposes.
You are free to modify and extend it as needed.
