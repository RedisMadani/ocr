# Chinese and English OCR

This is a script for performing optical character recognition (OCR) on Chinese and English text using the Tesseract OCR engine. It provides a graphical user interface (GUI) built with PyQt5.

## Requirements

- Python 3.x
- PyQt5
- Tesseract OCR engine
- Tesserocr Python library
- Pretrained language models for Tesseract OCR

## Installation

1. Install Python 3.x: [Python Installation Guide](https://www.python.org/downloads/)
2. Install PyQt5:
   ```
   pip install PyQt5
   ```
3. Install Tesseract OCR:
   - Windows: Download the installer from the [Tesseract GitHub repository](https://github.com/UB-Mannheim/tesseract/wiki) and follow the installation instructions.
   - macOS: Install using Homebrew:
     ```
     brew install tesseract
     ```
   - Linux: Install using the package manager specific to your distribution. For example, on Ubuntu:
     ```
     sudo apt-get install tesseract-ocr
     ```
4. Install Tesserocr library:
   ```
   pip install tesserocr
   ```
5. Download the pretrained language models for Tesseract OCR. You can find them on the [official Tesseract GitHub repository](https://github.com/tesseract-ocr/tessdata/tree/4767ea922bcc460e70b87b1d303ebdfed0897da8). Place the downloaded language models in the `raw/models` directory.

## Usage

Run the script using the following command:

```
python script.py
```

The GUI window will appear, providing various options for performing OCR:

### File Menu

- **Open target folder ...**: Open the target folder where the OCR results will be saved.
- **Download pretrained language modules ...**: Open the webpage to download additional pretrained language models.
- **Open language modules ...**: Open the `raw/models` directory where the pretrained language models are stored.
- **Switch language ...**: Select a supported language for OCR.
- **Exit**: Close the application.

### Recognize Menu

- **From folder ...**: Recognize text from multiple images in a selected folder.
- **From single image ...**: Recognize text from a single selected image file.
- **From clipboard**: Recognize text from an image in the clipboard.

### Help Menu

- **Version and supported language**: Display the Tesseract OCR version, path to pretrained language models, and the list of supported languages.

## Note

- The GUI supports both Chinese and English languages for OCR.
- The script utilizes the `BatchOCR`, `SingleOCR`, and `ClipboardOCR` classes from the `ocr_wrapper` module.
- OCR progress is displayed using a progress bar and messages are shown in the message box.

## License

This script is released under the [MIT License](LICENSE).

Feel free to contribute or report issues on [GitHub](https://github.com/yourusername/your-repo).