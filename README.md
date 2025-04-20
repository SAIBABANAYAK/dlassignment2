# dlassignment2
# 🔤 Hindi Transliteration using Seq2Seq (PyTorch)

This project implements a character-level transliteration system from Latin-script Hindi to Devanagari using a Seq2Seq model (Encoder-Decoder) with PyTorch. It also includes an experimental setup for Hugging Face Transformers and datasets.

---

## 📁 Project Structure

transliteration_project/ │ ├── transliteration_seq2seq.py # Question 1: Seq2Seq implementation in PyTorch ├── hf_transformers_setup.py # Question 2: Hugging Face datasets and tokenizer example ├── hi.translit.sampled.dev.tsv # Validation dataset (TSV format) ├── README.md # This file

yaml
Copy
Edit

---

## 🧠 Question 1: Hindi Transliteration (PyTorch Seq2Seq)

### 🛠️ Model Architecture
- Character-level Encoder-Decoder
- GRU-based RNNs (can be swapped to LSTM or vanilla RNN)
- Teacher forcing during training
- Supports prediction and accuracy evaluation

### 📄 Data Format (`hi.translit.sampled.dev.tsv`)
Each line contains:
<target_devanagari> <tab> <source_latin> <tab> <frequency>

markdown
Copy
Edit

### ✅ How to Run

1. Install dependencies:
   ```bash
   pip install torch numpy
Run training/prediction:

bash
Copy
Edit
python transliteration_seq2seq.py
Sample output:

yaml
Copy
Edit
Input: namaste | Target: नमस्ते | Predicted: नमस्ते
🤗 Question 2: Hugging Face Transformers Setup
🔍 Purpose
This script demonstrates loading datasets and tokenizers using Hugging Face libraries.

✅ Installation
bash
Copy
Edit
pip install transformers datasets
✨ Example Usage
python
Copy
Edit
from datasets import load_dataset
from transformers import GPT2Tokenizer

dataset = load_dataset("wikitext", "wikitext-2-raw-v1")
tokenizer = GPT2Tokenizer.from_pretrained("gpt2")
📝 Notes
You can easily extend this project by adding BLEU score, attention mechanism, or Transformer-based models.

Fine-tuning transformer models on transliteration tasks is also possible using the Hugging Face pipeline.

📌 Requirements
Python 3.7+

PyTorch

transformers

datasets (for Hugging Face)

📧 Contact
Feel free to open an issue or reach out if you have questions!

📜 License
MIT License. Free to use and modify.

yaml
Copy
Edit

---

Let me know if you want to split this into two separate `README.md` files or generate `.py` files too!
