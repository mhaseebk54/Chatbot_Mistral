# Mistral Chatbot

This project demonstrates a simple **offline AI chatbot** built using the **GPT4All** Python library and the **Mistral-7B-Instruct** model (`mistral-7b-instruct-v0.1.Q4_0.gguf`).  
The notebook includes topic explanation, text summarization, translation, and an interactive chatbot loop.

---

## 🚀 Features

- Uses the **gpt4all** library for local inference  
- Loads the **Mistral-7B-Instruct** offline model  
- Generates beginner-friendly topic explanations  
- Summarizes text into a single line  
- Translates text into another language  
- Simple chatbot loop using terminal input  

---

## 📦 Installation

1. Install GPT4All:
```bash
pip install gpt4all


Place the model file (mistral-7b-instruct-v0.1.Q4_0.gguf) inside your GPT4All models folder.

🎯 Usage
Load the Model
from gpt4all import GPT4All

model = GPT4All('mistral-7b-instruct-v0.1.Q4_0.gguf')

Topic Explanation
topic = "What is Artificial Intelligence in simple words?"
output = model.generate(f"Give me {topic} beginner-friendly explanation")
print("Topic:", output)

Summarization
summarize = """
Machine learning is a field of artificial intelligence that ...
"""
summary = model.generate(f"Make this one-line sentence: {summarize}")
print("Summary:", summary)

Interactive Chat Loop
while True:
    question = input("You: ")
    if question.lower() == "bye":
        break
    answer = model.generate(question)
    print("AI bot:", answer)

Translation and Summary
paragraph = "Data science is an interdisciplinary field that uses..."
summary = model.generate(f"Make a one-line summary: {paragraph}")
translate = model.generate(f"Translate in Urdu: {paragraph}")

print("Summary:", summary)
print("Translation:", translate)

📝 Notes

Runs fully offline using GPT4All

The Mistral model is used for all text generation

Everything is executed inside the notebook

🛠️ Tech Stack

Python

GPT4All

Mistral-7B-Instruct model

Jupyter Notebook
pt4all
pip install gpt4all
