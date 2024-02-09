Scraper2.5.py

This Python script (Scraper2.5.py) is designed to scrape web content from a specified URL and save the text and images into a Microsoft Word document. It navigates through the website, visiting links found on the initial page, and captures text and images, organizing them neatly into a .docx file. This tool is particularly useful for compiling information from web pages into a single document for offline review, documentation, or archiving purposes.
Features

    Recursive Scraping: Automatically visits and scrapes content from all linked pages within the base URL domain.
    Content Extraction: Grabs text content and images, saving them into a structured Word document.
    Link Preservation: Captures and lists all hyperlinks found in the text content as plain text within the document.
    Error Handling: Provides feedback on inaccessible pages or failed content fetching attempts.
    Image Handling: Downloads and inserts images into the document, adjusting their width to maintain readability.

Requirements

Before running this script, ensure you have Python 3 installed on your system. Additionally, the script depends on several external libraries:

    requests for making HTTP requests.
    BeautifulSoup from bs4 for parsing HTML content.
    python-docx for creating and manipulating Word documents.

You can install these dependencies by running:

bash

pip install requests beautifulsoup4 python-docx

Usage

To use the script, follow these steps:

    Set the Target URL and Output File: Open the script and modify the url and output_file variables in the main function to reflect the website you wish to scrape and the desired name of the output Word document.

    python

url = 'https://example.com'
output_file = 'output.docx'

Run the Script: Execute the script from your command line or terminal:

bash

    python webscraper_to_docx.py

    Review the Document: Open the generated Word document to review the scraped content.

Customization

The script offers several points of customization:

    Filtering Links: Modify the is_valid_url method to adjust which links should be followed based on your requirements.
    Adjusting Image Size: Change the width of images in the save_image method to better fit your document layout preferences.
    Content Selection: Adjust the parse_content method to change which HTML elements are included in the Word document.

Limitations

    The script currently does not execute JavaScript, so content loaded dynamically via JavaScript will not be captured.
    Only images accessible via direct links are downloaded and included in the document.

Contributing

Contributions to enhance the functionality, improve efficiency, or extend the capabilities of this script are welcome. Please feel free to fork the repository, make your changes, and submit a pull request.
License

This script is provided under an open-source license. Please review the LICENSE file for more information.
