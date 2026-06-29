# LOSReader 3.0.0

This is a helper program for reading letters of support.

## Prerequisites
Install [Python](https://www.python.org/). Make sure the box that adds Python to your PATH is checked.

Install [Tesseract](https://github.com/UB-Mannheim/tesseract/wiki). Make sure Tesseract is added to your PATH.

## Installation
1. [Download](https://docs.github.com/en/get-started/start-your-journey/downloading-files-from-github) the files and unzip to your preferred location.

2. Open your terminal (Windows: PowerShell/Command Prompt, macOS: Terminal)

3. Navigate to the folder
```bash
cd path/to/project
```
4. Install dependencies

```bash
pip install -r requirements.txt
```
5. In the project folder, open \LOSReader\ingestion\ocr.py in a text editor. Edit:
```
pytesseract.pytesseract.tesseract_cmd = r"path/to/tesseract.exe"
```
so that it points to the path to tesseract.exe and save.
## Usage
Files are stored in three main folders: **samples, results, and cache.**

+ samples - Save the letters to this folder. The program can handle PDF and image files 
+ results - This is where the output files are stored in PDF format.
+ cache - This is where the raw text extracted from the original file is stored.

These folders can be emptied after you are done reviewing a letter. Note: these folders will not appear until you run the program for the first time.

To run this program, open your terminal and make sure your working directory is pointed towards the project folder.
```bash
cd path/to/project
```
### Running the program interactively:
```bash
python run_checker.py
```
![options](/images/photo1.png)

### Running the program statically
```bash
python run_checker.py <letter.pdf> insurnace 
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)