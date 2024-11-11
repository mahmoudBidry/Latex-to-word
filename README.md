# LaTeX to Word Converter

This Jupyter Notebook provides a streamlined solution for converting LaTeX files (`.tex`) to Word documents (`.docx`). The converter supports the following features:

- **Image Support**: Integrates images from the LaTeX document into the Word output, maintaining the same paths to ensure images appear in the Word document as they do in LaTeX.
- **Table Conversion**: Converts LaTeX tables into Word tables with bordered cells, improving readability and aligning with Word formatting standards.
- **Text Formatting**: Sets the entire Word document to a consistent font style (Times New Roman) and size (12 pt), ensuring a professional and uniform appearance.

## Requirements

Ensure the following Python libraries are installed to run this notebook:

- `pypandoc`
- `python-docx`
- `pandas` (for table handling)
- `re` (for text processing)

You can install the dependencies via pip:

```bash
pip install pypandoc python-docx pandas
