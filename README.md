# Search Snippet - LinkedIn Profile Scraper

A robust, asynchronous Python script designed to bulk search and extract LinkedIn profile details using DuckDuckGo Search. It processes Excel files containing LinkedIn URLs and retrieves snippets including titles, URLs, and descriptions.

## Author
Vishnu Bhagirathan 

## Features

- **Asynchronous Processing:** Utilizes `asyncio` for concurrent searches, optimized for speed and stability.
- **User-Friendly Interface:** A welcome screen and prompts for file name and retry counts.
- **Smart Retries:** Includes built-in retry logic with increasing delays to handle rate limits and temporary blocks.
- **Multiple Search Strategies:** Employs primary and fallback search queries to maximize result accuracy.
- **Data Persistence:** Automatically saves progress to Excel every 3 processed entries to prevent data loss.
- **Multi-Sheet Support:** Automatically detects and processes all sheets within the input Excel file.
- **Automated Logging:** Updates session logs and changelogs upon completion.

## Prerequisites

- Python 3.7+
- An input Excel file with a column named `LinkedIn URL` (or the first column should contain the URLs).

## Installation

1. Clone or download this repository.
2. Install the required Python dependencies:

```bash
pip install -r requirements.txt
```

## Usage

1. Place your input Excel file in the project directory.
2. Run the script:

```bash
python scrape.py
```
3. The script will prompt you for the following information:
   - File name with extension (e.g., `Live.xlsx`).
   - Number of retries per link.
   - Number of retries per sheet.

4. The script will then process the file and generate output files.

## Output

The script will generate separate output files for each sheet processed, named:
`live_processed_<SheetName>.xlsx`

These files will contain a new column `Search Result Detail` with the retrieved information or error details if a search fails after all retries.

## Technical Details

- **Concurrency:** Processes 3 profiles at a time (chunk size) to balance speed and avoid aggressive rate-limiting.
- **Delays:** Implements random delays between 5-8 seconds per search to mimic human behavior and maintain search stability.
- **Persistence:** If a processed file already exists (e.g., from a previous interrupted run), the script will resume from where it left off.