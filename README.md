# BC Data Extraction: MarkItDown + Grok

A simple, modern Streamlit app to extract text from Microsoft Office files (Word, Excel, PowerPoint), PDFs, and images (JPG/PNG). Uses [MarkItDown](https://github.com/markitdown/markitdown) for document text extraction and [xAI Grok Vision](https://x.ai/) for image understanding and OCR.

---

## Features

- **Extracts text from DOCX, PPTX, XLSX, PDF using MarkItDown**
- **Extracts and OCRs images (JPG/PNG or embedded in documents) using Grok Vision**
- **Displays results in a clean, organized UI**
- **Handles errors and missing dependencies gracefully**

---

## Quickstart (For Beginners)

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/bc_data_extraction_markitdown_grok.git
cd bc_data_extraction_markitdown_grok
```

### 2. Create and Activate a Virtual Environment (Recommended)
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

**If you want to support all Office/PDF/image types:**
```bash
pip install 'markitdown[all]' openai streamlit python-docx python-pptx openpyxl pymupdf
```

### 4. Set Up Your xAI API Key
- Get an API key from [xAI](https://console.x.ai/)
- Set it in your environment:
```bash
export XAI_API_KEY=your_xai_api_key_here
```
- (On Windows, use `set` instead of `export`)

### 5. Run the App
```bash
streamlit run app.py
```
- Open the URL shown in your terminal (usually http://localhost:8501)

---

## Usage
- Upload DOCX, PPTX, XLSX, PDF, JPG, or PNG files.
- The app will extract all text and any images, OCR images with Grok, and display results in expandable sections.
- Errors and missing dependencies will be shown in the UI.

---

## Troubleshooting
- **Missing Dependency:** If you see a message about a missing package (e.g., `python-docx`, `fitz`), install it with pip.
- **No OCR Output:** If Grok returns no text, check your API key, quota, and image quality. Not all images will yield results.
- **API Key Issues:** Ensure your API key is set and has vision access.

---

## Project Structure
```
├── app.py           # Main Streamlit app
├── requirements.txt # Python dependencies
├── README.md        # This file
├── .env             # (Optional) for environment variables
```

---

## License

MIT License

Copyright (c) 2025 Camilo Serna Zamora

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
