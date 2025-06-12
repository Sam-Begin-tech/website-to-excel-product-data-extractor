# 🛒 Product Data Extractor from Website to Excel (LLM-Powered)

This is a Python-based prototype that automatically crawls a website, extracts product-related information using an AI language model, and saves the results into an Excel spreadsheet.

It’s designed to be simple and beginner-friendly, using modular Python code and LLM (Large Language Model) via LangChain + Ollama for intelligent text understanding.

---

## ✨ What It Does

✅ Crawls a website and visits all internal links  
✅ Extracts all visible text from each page  
✅ Cleans the content by removing unnecessary text like “Login”, “Add to Cart”, etc.  
✅ Breaks large content into chunks  
✅ Uses a Language Model (like Gemma via Ollama) to extract:
- Product Name
- MRP (Maximum Retail Price)
- Selling Price  
✅ Parses LLM output into clean structured JSON  
✅ Removes duplicate products  
✅ Saves the final list into an Excel file

---

## 🖼️ Example Output (Excel Columns)

| ProductName         | MRP    | sellingPrice |
|---------------------|--------|---------------|
| Sunflower Oil 1L    | ₹200   | ₹180          |
| Aashirvaad Atta 5kg | ₹300   | ₹270          |

---

## 🧠 Tech Stack

- Python 3
- requests + BeautifulSoup – for web crawling
- re + json – for cleaning and formatting
- LangChain + Ollama – for LLM-driven extraction
- pandas + numpy – for data processing
- Excel Export – via pandas `.to_excel()`

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Ollama installed locally with model like `gemma2:2b`
- LangChain library
- pandas, numpy, beautifulsoup4


| File              | Purpose                              |
| ----------------- | ------------------------------------ |
| product_data_extraction.ipynb           | Main logic for crawling & extraction |
|data_extraction.ipynb |  Notebook showing your initial prototyping|
| README.md         | This documentation                   |
| products.xlsx | Output file (auto-generated)         |


---

## 🧠 Ollama Installation & Model Setup

This project uses Ollama to run a local LLM (Large Language Model) that extracts product details from raw webpage text.

### 📥 Step 1: Install Ollama

Ollama allows you to run open-source LLMs locally on your machine.

Install it from the official site:

🔗 [https://ollama.com/download](https://ollama.com/download)

Choose the version for:

* Windows
* macOS
* Linux (Ubuntu/Debian via terminal)

After installation, make sure the ollama command is available in your terminal:

```bash
ollama --version
---

## 🧠 Ollama Installation & Model Setup

This project uses Ollama to run a local LLM (Large Language Model) that extracts product details from raw webpage text.

### 📥 Step 1: Install Ollama

Ollama allows you to run open-source LLMs locally on your machine.

Install it from the official site:

🔗 [https://ollama.com/download](https://ollama.com/download)

Choose the version for:

* Windows
* macOS
* Linux (Ubuntu/Debian via terminal)

After installation, make sure the ollama command is available in your terminal:

```bash
ollama --version
```

If this works, you're ready to run local models!

---

### 📦 Step 2: Pull the Required Model

This project uses the Gemma 2B model. Pull it using:

```bash
ollama pull gemma2:2b
```

Wait for the model to download (this may take a few minutes). Once completed, Ollama can run it locally in the background.

You can test it with:

```bash
ollama run gemma2:2b
```

---

📝 Note:
You can replace gemma2:2b with any other LLM you prefer (e.g., phi3, llama3, etc.), as long as it's compatible with your LangChain or inference code.

---
```

If this works, you're ready to run local models!

---

### 📦 Step 2: Pull the Required Model

This project uses the Gemma 2B model. Pull it using:

```bash
ollama pull gemma2:2b
```

Wait for the model to download (this may take a few minutes). Once completed, Ollama can run it locally in the background.

You can test it with:

```bash
ollama run gemma2:2b
```

---

📝 Note:
You can replace gemma2:2b with any other LLM you prefer (e.g., phi3, llama3, etc.), as long as it's compatible with your LangChain or inference code.

---

---

## 🌐 Demo Website Used

This prototype was tested using the following publicly accessible e-commerce site:

🔗 [https://edenmart.in/](https://edenmart.in/)

It was used as an example to:

* Demonstrate product data crawling and extraction
* Validate LLM-based parsing of pricing details
* Export a real-world dataset into Excel

⚠️ Note:
This tool is intended solely for educational and demonstration purposes. It does not store, misuse, or distribute any data obtained from the target website. Users are strongly advised to review and comply with the website’s robots.txt file and Terms of Service before applying this tool to any external domain.

---

Install dependencies:

```bash
pip install requests beautifulsoup4 langchain langchain-community pandas numpy openpyxl
