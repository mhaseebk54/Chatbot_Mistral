# Chatbot_Mistral
This project demonstrates a simple chatbot built using the GPT4All Python library and the Mistral-7B-Instruct model file (mistral-7b-instruct-v0.1.Q4_0.gguf).
The notebook includes topic explanation, summarization, translation, and an interactive chatbot loop.

📌 Features (Only What Exists in the File)

✔ Install and use gpt4all
✔ Load Mistral-7B-Instruct offline model
✔ Generate topic-based explanation
✔ Summarize text into a single line
✔ Translate text (English → another language)
✔ Interactive chatbot loop using terminal input

📁 Notebook Contents
Section	Description
Install Dependencies	!pip install gpt4all
Load Model	GPT4All('mistral-7b-instruct-v0.1.Q4_0.gguf')
Topic Explanation	Generates beginner-friendly answer
Summarization	Converts paragraph into 1-line summary
Chat Loop	User enters text → model generates response
Translation	Translates a paragraph
🔧 Installation
1️⃣ Install gpt4all
pip install gpt4all

2️⃣ Make sure the model file exists

Your notebook uses:

mistral-7b-instruct-v0.1.Q4_0.gguf


Place this file inside your GPT4All models folder.

🚀 Usage
Load the Model
from gpt4all import GPT4All
model = GPT4All('mistral-7b-instruct-v0.1.Q4_0.gguf')

Generate Topic Explanation
topic = "What is Artificial Intelligence in simple words?"
output = model.generate(f"give me {topic} beginner-friendly explanation")
print("Topic :", output)

Summarization
summarize = """
Machine learning is a field of artificial intelligence that ...
"""
summary = model.generate(f"make this one line sentence {summarize}")
print("Summary:", summary)

Interactive Chat Loop
while True:
    question = input("You : ")
    if question.lower() == "bye":
        break
    answer = model.generate(question)
    print("Ai bot:", answer)

Translation + Summary
paragraph="Data science is an interdisciplinary field that uses..."
summary = model.generate(f"Make a one-line summary {paragraph}")
translate = model.generate(f"Translate in Urdu {paragraph}")

print("Summary :", summary)
print("Translation :", translate)

📜 Notes

The project uses only GPT4All local inference (no internet required).

The Mistral model runs fully offline.

Everything is executed inside the notebook..
