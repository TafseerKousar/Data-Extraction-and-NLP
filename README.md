# Data-Extraction-and-NLP
Instructions Documentation: Data Extraction and NLP Project

## Overview
This project involves extracting and analyzing articles from URLs, performing sentiment analysis, and calculating various textual metrics. The program reads a list of URLs from an input file, extracts article content, cleans the text, and computes scores such as polarity, subjectivity, FOG index, average sentence length, and more. Results are saved to an output file.
________________________________________
## Dependencies and Setup
Required Libraries
●	pandas: For reading and writing Excel files.
●	requests: For making HTTP requests to URLs.
●	bs4 (BeautifulSoup): For parsing HTML and extracting article content.
●	nltk: For text processing tasks like tokenization and stop words filtering.
●	numpy: For numerical computations.
●	urllib3: For setting retry mechanisms on requests.
●	re: For handling regular expressions in text processing.
●	os: For directory and file path operations.
●	time: For managing wait times and delays in processing.
●	random: For generating random values as needed.
●	datetime: For handling date and time in logging or timestamping.
●	shutil: For file operations such as moving files.
________________________________________
## Approach and Methodology
Step-by-Step Process:
##### 1.	Initialize TextAnalyzer Class:
o	Sets up retry mechanisms for network requests, output directories, and loads necessary word lists for analysis.
##### 2.	Data Extraction and Processing:
o	Reads URLs or input texts.
o	Extracts article text and cleans it for analysis.
##### 3.	Text Cleaning & Tokenization:
o	Converts text to lowercase, removes punctuation, and tokenizes.
o	Filters out stop words.
##### 4.	Sentiment and Readability Analysis:
o	Sentiment Scores: Positive and negative word counts, polarity, and subjectivity scores.
o	Readability Metrics: Calculates FOG Index, word complexity, syllables, and sentence length metrics.
##### 5.	Save Results:
o	Compiles analysis results in a DataFrame and saves it to output_files/analysis_output.xlsx.
o	Any errors encountered during processing are logged in failed_urls.xlsx.
________________________________________
## Key Functions
Here’s a breakdown of each primary function used in the project:
●	create_directories: Creates necessary output directories.
●	read_file_with_encoding: Reads files with various encodings, handling Unicode errors.
●	load_stop_words: Loads and merges custom stop words and NLTK stop words.
●	extract_article: Retrieves the main content from a webpage, filtering unwanted HTML elements.
●	clean_text: Cleans and tokenizes text for analysis.
●	analyze_text: Computes various metrics for text sentiment and readability analysis.
●	safe_file_write: Writes results to an Excel file, retrying if permission errors occur.
________________________________________
## Output Details
The final output file includes these metrics:
●	POSITIVE_SCORE: Positive word count.
●	NEGATIVE_SCORE: Negative word count.
●	POLARITY_SCORE: Overall sentiment (-1 to +1).
●	SUBJECTIVITY_SCORE: Measure of subjectivity.
●	FOG_INDEX: Readability score.
●	AVG_WORD_LENGTH: Average word length.
