The code performs text extraction and summarization from a webpage. Here’s a step-by-step breakdown:

1. Import Libraries:
   - `BeautifulSoup` (`bs4`) for HTML parsing.
   - `urllib` for fetching web content.
   - `re` for regular expressions to clean text.
   - `nltk` for natural language processing tasks.

2. Download NLTK Resources:
   - Downloads `punkt` for tokenization and `stopwords` for filtering common words.

3. Fetch and Parse Webpage:
   - Fetches HTML content from a specified URL.
   - Parses the HTML using BeautifulSoup to extract the text from `<p>` (paragraph) tags.

4. Clean and Process Text:
   - Removes square brackets, extra spaces, and special characters.
   - Normalizes text by removing digits and non-alphabetic characters.
   - Tokenizes text into sentences and words.
   - Removes stop words and calculates word frequencies.

5. Summarize Text:
   - Normalizes word frequencies.
   - Scores sentences based on the sum of word frequencies.
   - Uses `heapq.nlargest()` to find the top 7 sentences with the highest scores and combines them into a summary.

