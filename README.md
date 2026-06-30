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
so that it points to tesseract.exe and save.
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

Choose the number that corresponds to your desired insurance.

![letter.pdf](/images/photo2.png)

Specify the name of the input file.

### Running the program statically
Alternatively, here is an identical way to run the program.
```bash
python run_checker.py letter.pdf --insurance 1
```
## License
Copyright (c) 2026 Daniel Qi

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