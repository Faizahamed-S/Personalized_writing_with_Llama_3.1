# 🦙 Personalized Writing with Llama

This project is a small experimental playground where I fine-tuned a Llama-based model on a custom dataset to generate personalized writing in a specific tone and style.

The goal was simple:

> Can we make a base LLM write more like *us* using lightweight fine-tuning?

---

## 📌 What This Project Does

- Uses a custom JSONL dataset (`Data_1.jsonl`)
- Fine-tunes a Llama model using parameter-efficient techniques
- Trains the model to generate writing in a personalized tone
- Runs inside a Jupyter notebook workflow

This is not a production system.  
It is an exploration into LLM customization and style conditioning.

---

## 🗂 Project Structure
├── Data_1.jsonl
├── Personalized_Writing_LLM.ipynb
└── README.md


### `Data_1.jsonl`

Custom dataset used for training.  
Each entry follows instruction-style formatting suitable for supervised fine-tuning.

### `Personalized_Writing_LLM.ipynb`

Notebook containing:
- Model loading
- Dataset preprocessing
- Fine-tuning setup
- Training loop
- Inference examples

---

## 🧠 Core Idea

Instead of prompting repeatedly to mimic a tone, we:

1. Provide examples of writing style.
2. Format them as instruction-response pairs.
3. Fine-tune the base Llama model.
4. Generate responses that naturally follow the learned style.

This helps:
- Reduce prompt engineering effort
- Improve stylistic consistency
- Create a semi-personal writing assistant

---

## ⚙️ Tech Stack

- Llama (open-source LLM)
- Hugging Face Transformers
- PEFT / LoRA (parameter-efficient fine-tuning)
- PyTorch
- Jupyter Notebook

---

## 🚀 How It Works (High-Level)

1. Load base Llama model.
2. Apply LoRA adapters for efficient training.
3. Feed custom JSONL dataset.
4. Train on style-conditioned instruction format.
5. Generate new text in the learned style.

---

## 🧪 Why This Matters

This experiment demonstrates:

- How small datasets can meaningfully shape LLM output
- How personalization does not require full fine-tuning
- How developers can build domain- or identity-specific assistants

This is a stepping stone toward:
- Resume tailoring assistants
- Custom tone-based content generators
- Personal knowledge-based agents

---

## 🔮 Future Improvements

- Add evaluation metrics (perplexity / BLEU / style similarity)
- Increase dataset size
- Add RAG for memory grounding
- Deploy as API

---

## 📜 Note

This project is experimental and intended for learning and exploration.
