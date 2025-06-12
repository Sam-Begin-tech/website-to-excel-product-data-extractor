# website-to-excel-product-data-extractor

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

Install dependencies:

```bash
pip install requests beautifulsoup4 langchain langchain-community pandas numpy openpyxl
