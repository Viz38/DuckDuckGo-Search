# CHANGELOG
All notable changes to this project are documented here.
## [2026-01-16] Added terminal clear on program start
- [modify]: `scrape.py`
- Reason: To clear the terminal as soon as the program runs, ensuring a clean display for the UI.
- Related tasks/tests: None

## [2026-01-16] Added .gitignore
- [create]: `.gitignore`
- Reason: To ignore .xlsx and .csv files from version control.
- Related tasks/tests: None

## [2026-01-16] Enhanced UI instructions
- [modify]: `scrape.py`
- Reason: Provided more detailed instructions in the welcome screen and input prompts for better user guidance.
- Related tasks/tests: None

## [2026-01-16] Improved user interface and input collection
- [modify]: `scrape.py`
- Reason: To enhance user experience by adding a welcome screen and prompting for file name, retries per link, and retries per sheet.
- Related tasks/tests: None

## [2026-01-15] Updated retry logic in scrape.py
- [modify]: `scrape.py`
- Reason: Implemented a retry mechanism for processing sheets, limiting attempts to 2 and displaying the current pass count.
- Related tasks/tests: None

## [2026-01-15] Added requirements.txt and updated README.md
- [create]: `requirements.txt`
- [modify]: `README.md`
- Reason: To streamline the installation process and ensure all dependencies are managed in one place.
- Related tasks/tests: None