# PDF-Outline-Extractor-Round-1B
# 📘 PDF Outline Extractor

A Python tool that automatically extracts **hierarchical document outlines** from PDFs, generating structured Table of Contents with heading levels and page numbers in **JSON, HTML**, and **CSV** formats.

---

## 🚀 Features

- **Multi-strategy detection**: Combines pattern matching, font analysis, and position detection
- **Hierarchical structure**: Identifies H1, H2, H3 heading levels automatically
- **Multiple output formats**: JSON, HTML reports, and CSV summaries
- **Batch processing**: Handle single files or entire directories
- **Fast & reliable**: Processes documents in milliseconds with high accuracy
- **Robust filtering**: Removes false positives and body text automatically

---

## 📋 Requirements

- Python 3.8 or higher
- PyMuPDF (`fitz`)

---

## 🛠️ Installation

### Clone the Repository

```bash
git clone https://github.com/KamalKumarMachireddy/PDF-Outline-Extractor-Round-1A.git
cd PDF-Outline-Extractor-Round-1A
Install Dependencies
bash
Copy
Edit
pip install PyMuPDF==1.23.14
Or use:

bash
Copy
Edit
pip install -r requirements.txt
🎯 Quick Start
Process a Single PDF
bash
Copy
Edit
python simple_pdf_processor.py sample.pdf
Process Multiple PDFs in a Directory
bash
Copy
Edit
python batch_pdf_processor.py --input ./pdfs --output ./results
Use in Your Python Code
python
Copy
Edit
from universal_pdf_extractor import UniversalPDFOutlineExtractor

extractor = UniversalPDFOutlineExtractor(debug=True)
result = extractor.extract_outline("document.pdf")

print(f"Title: {result['title']}")
print(f"Found {len(result['outline'])} headings")

for heading in result['outline']:
    print(f"{heading['level']} - Page {heading['page']}: {heading['text']}")
📊 Output Example
json
Copy
Edit
{
  "title": "Understanding AI Systems",
  "outline": [
    {
      "level": "H1",
      "text": "1. Introduction",
      "page": 1
    },
    {
      "level": "H2", 
      "text": "What is Artificial Intelligence?",
      "page": 2
    },
    {
      "level": "H3",
      "text": "Machine Learning Basics", 
      "page": 3
    }
  ],
  "method": "structure_analysis"
}
📁 Project Structure
bash
Copy
Edit
pdf-outline-extractor/
├── universal_pdf_extractor.py    # Main extraction engine
├── batch_pdf_processor.py        # Batch processing tool
├── simple_pdf_processor.py       # Single file processor
├── test.pdf                      # Sample PDF
├── README.md                     # Project documentation
└── output/                       # Generated reports
🎨 Command Line Options
Single File
bash
Copy
Edit
python simple_pdf_processor.py <pdf_file> [output_file]
Batch Processing
bash
Copy
Edit
python batch_pdf_processor.py [options]
Options:

--input, -i: Input directory (default: current directory)

--output, -o: Output directory (default: output)

--debug, -d: Enable debug output

📈 Performance
Speed: Processes most documents in under 0.1 seconds

Accuracy: Multi-strategy approach ensures high detection rates

Scalability: Efficiently handles documents up to 50 pages

Memory: Optimized for low memory usage

🔧 Supported Document Types
✅ Academic papers
✅ Technical documentation
✅ Business reports
✅ Books and chapters
✅ Research papers
✅ User manuals
✅ Any structured PDF document

🎯 Use Cases
Perfect for:

Researchers: Generate TOCs for paper collections

Students: Navigate complex academic documents

Content Managers: Index document libraries

Developers: Automate document analysis workflows

Digital Libraries: Create searchable document indexes

🛡️ Detection Strategies
The extractor uses three complementary strategies:

Pattern Matching: Detects numbered sections and common headings

Font Analysis: Identifies headings by size, weight, and formatting

Position Analysis: Detects isolated text with proper spacing

📝 Output Formats
JSON: Structured data for programmatic use

HTML: Beautiful reports with navigation

CSV: Spreadsheet-compatible summaries

🐛 Troubleshooting
Common Issues:

❗ "No PDF files found!"

Check if PDF files exist in the directory

Ensure files have .pdf extension

❗ PyMuPDF errors

bash
Copy
Edit
pip install --upgrade pip
pip install PyMuPDF==1.23.14
❗ Large PDF memory issues

The extractor auto-limits to 50 pages

Split documents if needed

Test Installation
python
Copy
Edit
import fitz
print("PyMuPDF version:", fitz.__doc__)
print("Installation successful!")
📊 Example Results
Processing 2 PDFs with 88 total headings:

✅ 100% success rate
⚡ 0.07s total processing time
📈 44 headings average per document

🤝 Contributing
Fork the repository

Create a feature branch

Make your changes

Add tests if needed

Submit a pull request
.

🙏 Acknowledgments
Built with PyMuPDF for PDF processing

Inspired by the need for better document analysis tools

📞 Support
If you encounter any issues or have questions:

Open an issue on GitHub

Refer to the troubleshooting section

Review example usage in the code

