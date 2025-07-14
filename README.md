# Docling Project

A comprehensive document processing project using the Docling library for advanced PDF parsing and OCR capabilities.

## 📁 Project Structure

```
Docling_project/
├── Notebook/
│   ├── basic_options.ipynb           # Simple conversion and multiple PDF processing
│   ├── advance_options.ipynb         # Advanced configuration and processing options
│   ├── advance_OCR_options.ipynb     # Enhanced OCR capabilities
│   ├── batch_process.ipynb           # Batch processing workflows
│   └── download_docling.ipynb        # Model downloading and setup
├── pdf/                              # Sample PDF documents for testing
├── output/                           # Processed document outputs
├── requirements.txt                  # Project dependencies
└── README.md                         # This file
```

## ✨ Features

- **Basic Document Conversion**: Simple PDF to Markdown conversion
- **Batch Processing**: Handle multiple PDF files simultaneously
- **Advanced OCR Options**: Enhanced text extraction with OCR capabilities
- **Local Model Support**: Download and use Hugging Face models locally
- **GPU/CPU Acceleration**: Configurable processing acceleration
- **Multiple Output Formats**: Markdown, JSON, HTML, and image extraction

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- pip package manager

### Installation

1. **Navigate to the project directory:**
```bash
cd Docling_project
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

### Quick Start

#### Basic Document Conversion
```python
from docling.document_converter import DocumentConverter

# Simple conversion
converter = DocumentConverter()
doc = converter.convert("path/to/document.pdf").document
markdown_output = doc.export_to_markdown()
print(markdown_output)
```

#### Download Models (Recommended)
For better performance, download models locally by running the `download_docling.ipynb` notebook:

```python
from docling.utils.model_downloader import download_models
from pathlib import Path

# Download models to local directory
download_models(output_dir=Path('local_path'))
```

## � Notebook Guide

### 1. `download_docling.ipynb`
Start here to download required models from Hugging Face for offline processing.

### 2. `basic_options.ipynb`
Learn the fundamentals:
- Simple PDF to Markdown conversion
- Processing multiple PDF files
- Using locally downloaded models
- GPU/CPU acceleration options

### 3. `advance_options.ipynb`
Explore advanced features:
- Custom configuration options
- Advanced processing parameters
- Performance optimization

### 4. `advance_OCR_options.ipynb`
Master OCR capabilities:
- Enhanced text extraction
- OCR parameter tuning
- Handling complex document layouts

### 5. `batch_process.ipynb`
Process multiple documents efficiently:
- Batch processing workflows
- Error handling
- Output management

## 📋 Dependencies

- **docling==2.31.0** - Core document processing library

## 🚀 Performance Tips

1. **Download models locally** using `download_docling.ipynb` for faster processing
2. **Use GPU acceleration** when available for large documents
3. **Batch process** multiple documents for efficiency
4. **Configure OCR settings** based on document type and quality

## 🐛 Troubleshooting

### Common Issues:
- **Model download fails**: Check internet connection and disk space
- **GPU not detected**: Ensure CUDA is properly installed
- **OCR accuracy low**: Adjust OCR parameters or use higher quality PDFs

### Getting Help:
- Check the individual notebooks for detailed examples
- Review the Docling documentation
- Verify all dependencies are installed correctly

## 📄 License

This project is for personal use and development purposes.
