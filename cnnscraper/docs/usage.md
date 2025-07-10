# Usage

The `cnnscraper.py` script provides a straightforward way to collect news data from CNN.

## Data Output

After successfully running the script, two main outputs are generated in your project's root directory:

1.  **`data.csv`**: A CSV file containing the scraped news article information.
    Each row in `data.csv` includes the following columns:
    *   `news_headline`: The main headline of the news article.
    *   `news_content`: The full text content of the article's paragraphs.
    *   `img_description`: The alternative text (description) of an associated image (usually the first found).
    *   `img_link`: The original URL of the associated image.
    *   `local_path`: The local path where the image is saved (e.g., `article_images/image_name.jpg`).

    ### Dataset Example

    A snippet of the generated `data.csv` file:

    ![Dataset screenshot](img/datacnn.png)

2.  **`article_images/` directory**: This folder is created to store all downloaded images associated with the scraped articles. Images are named based on their original filenames (sanitized) and saved as `.jpg`.

## Script Interaction

When you run `cnnscraper.py`, you will be prompted to interact with the script:

```
Available Dates:
1. February 01, 2023
2. March 15, 2023
...
Choose one date at a time where you want to get news for from the available options(eg 1, 2, 3):
```
Enter the number corresponding to the date you wish to scrape. After selecting, you'll be asked:
```
Do you want to select more dates? (yes/no):
```
Type `yes` to select another date or `no` to proceed with scraping for the currently selected dates.

## Error Handling

*   If an image fails to download, an error message will be printed to the console, but the script will continue.
*   If the `data.csv` file already exists from a previous run, it will be automatically overwritten to ensure fresh data.