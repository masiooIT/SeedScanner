# SeedScanner


![alt text](https://raw.githubusercontent.com/masiooIT/SeedScanner/main/seedscanner.webp)

SeedScanner is a powerful tool designed to scan files on a selected drive for seed phrases and keywords. It supports various file types, including text files, PDFs, Office documents, images (with OCR support), and archives. The software allows users to customize their scanning options, such as file size limits and minimum image dimensions, making it a versatile and robust tool for security and data management tasks.

## Features

- **Multi-threaded Scanning**: Utilizes worker threads to perform efficient and fast scanning.
- **Customizable Scanning Options**: Choose file types to scan (text, images, archives) and set file size limits.
- **OCR Support**: Scans images for text using Optical Character Recognition (OCR) with support for multiple languages.
- **Archive Extraction**: Automatically extracts and scans files within ZIP, TAR, and 7z archives.
- **Seed Phrase and Keyword Detection**: Identifies seed phrases and keywords in various file formats.
- **Detailed Progress Logging**: Displays progress and detailed logging of the scanning process.
- **Scan Results and Statistics**: Generates comprehensive reports on scan results and file statistics.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/seedscanner.git
    cd seedscanner
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Ensure required tools are installed**:
    - Node.js
    - 7-Zip (ensure the 7z executable is in your PATH)

## Usage

1. **Run SeedScanner**:
    ```bash
    node app.js
    ```

2. **Follow the prompts**:
    - Select the drive to scan.
    - Choose the file types to scan.
    - (If scanning images) Set minimum image dimensions.
    - Set the maximum file size for scanning.
    - Specify the OCR language.

3. **View the results**:
    - Scan progress will be displayed in the console.
    - Detailed results and statistics will be saved in `scan_results.txt` and `scan_statistics.txt`.

## Example

Here's an example of what using SeedScanner might look like in the console:

```sh
? Select the drive to scan: C:
? Select the file types to scan (at least one): 
  ◉ Text (including PDF, Office support)
  ◉ Images (OCR)
  ◉ Archives
? Enter the minimum image width (px): 100
? Enter the minimum image height (px): 100
? Enter the maximum file size to include in the scan (MB): 50
? Enter the OCR language code (e.g., eng, ita): eng

Indexing files...
Found 13906 files.
File statistics:
  .txt: 5000 files (35.96%)
  .pdf: 3000 files (21.58%)
  .docx: 2000 files (14.39%)
  .xlsx: 1000 files (7.19%)
  .jpg: 2906 files (20.88%)

Progress: 25.00%
...
