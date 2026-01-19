The `scrape.py` script has been facing accuracy issues with its search results. The root cause of the problem lies in the broadness of the search queries, which sometimes returns irrelevant information instead of the desired LinkedIn profiles.

To address this, I have implemented a more targeted search strategy. By extracting the person's name from the LinkedIn URL and including it in the search query, the script can now perform more specific searches, significantly improving the relevance and accuracy of the results.

Here is a summary of the key changes:

- **Refined Search Queries:** The script now constructs more detailed search queries by combining the person's name with the LinkedIn profile slug, leading to more accurate and relevant search results.
- **Improved Name Extraction:** I have enhanced the `extract_linkedin_id` function to reliably extract the person's name from the URL, providing more context for the search query.
- **Error Handling:** The script is now more resilient to errors, with improved error handling that ensures smoother execution even when faced with unexpected search results.

These improvements have been tested on a sample of the data, and the results show a significant increase in accuracy. The script is now better equipped to handle large-scale data processing tasks with greater precision and reliability.
