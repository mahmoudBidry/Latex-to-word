# LaTeX to Word Converter

This Jupyter Notebook provides a streamlined solution for converting LaTeX files (`.tex`) into Word documents (`.docx`). The conversion preserves essential elements, such as images, tables, and consistent text formatting, making it easier to produce a polished Word document from a LaTeX source.

## Features

- **Image Integration**: Incorporates images from the LaTeX file into the Word document, maintaining the original image paths for accurate rendering.
- **Table Conversion**: Transforms LaTeX tables into bordered Word tables, enhancing readability and maintaining table structure.
- **Text Formatting**: Formats the entire document in Times New Roman, 12 pt font for a cohesive and professional appearance.
- **Reference Formatting**: Supports reference formatting through an IEEE citation style (`ieee.csl`). For other citation styles, you can download the appropriate `.csl` file from the [CSL GitHub Repository](https://github.com/citation-style-language/styles) and replace `ieee.csl` with the desired style file.

## Requirements

Ensure the following Python libraries are installed:

- `pypandoc`
- `python-docx`
- `re`

Install the dependencies with:

```bash
!wget https://github.com/jgm/pandoc/releases/download/3.1.6.1/pandoc-3.1.6.1-1-amd64.deb
!dpkg -i pandoc-3.1.6.1-1-amd64.deb

!pip install python-docx
```


## Usage

### Step 1: Set Up Your Google Drive Folder Structure

1. Organize your project in Google Drive with the same folder structure you used in Overleaf, including the `.tex` file, `.bib` file, images, and the citation style file (`.csl`).
2. Adapt the following four lines in the notebook to match your project folder and file names:

   ```python
   latex_dir = "your_drive_folder_path/"
   csl_file = os.path.join(latex_dir, "ieee.csl")  # Change 'ieee.csl' if using a different citation style
   tex_file = os.path.join(latex_dir, "paper.tex") # Change 'paper.tex' to your LaTeX file name
   bib_file = os.path.join(latex_dir, "sample.bib") # Change 'sample.bib' to your bibliography file name
   ```

   Ensure these paths point to the correct directory and files on your Google Drive.

### Step 2: Run the Notebook

1. Place your LaTeX (`.tex`) file, bibliography (`.bib`) file, `ieee.csl` (or other citation style file), and any associated images in the Google Drive directory specified.
2. Run the notebook, which will:
   - Parse and convert LaTeX content (text, images, and tables) into Word.
   - Modify table structures to ensure consistent borders and alignment.
   - Apply the designated font and size across the entire Word document.
3. The output Word document (`output_with_borders.docx`) will be saved in the same directory as your LaTeX file.

> **Note:** The cleaner and more standardized your LaTeX code, the more accurate the Word conversion will be.

## License

This notebook is released under the MIT License.
