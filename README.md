# Map_Reduce_Assignment
This code is designed to perform several tasks related to processing text extracted from a PDF file, particularly from the "Harry Potter" PDF document. Here's an overview of the code and its functionality:

### 1. Text Extraction from PDF:

The code uses the PyMuPDF library (also known as "fitz") to extract text content from a provided PDF file (in this case, "Harry_Potter_(www.ztcprep.com).pdf").
It defines a function extract_text_between_markers that extracts text between specified start and end markers on each page of the PDF.

### 2. Marker-Based Text Extraction:

The extract_text_between_markers function takes as input the PDF file path, start marker, end marker, and an output file path.
It iterates through each page of the PDF, looking for the start marker.
Once the start marker is found, it starts accumulating text until it encounters the end marker on a page.
It then removes the text before the start marker and after the end marker.
The extracted text is saved to a text file with the specified output path.

### 3. Usage Example:

The code provides an example of how to use the extract_text_between_markers function to extract specific content from the PDF. Two separate extractions are demonstrated with different start and end markers.

### 4. English Word Validation:

After extracting text, the code validates the extracted words to ensure they are valid English words.
It uses the PyEnchant library to check if each word in the text is a valid English word.
Punctuation marks and special characters are removed from the words to avoid false positives.

### 5. Non-English Word Count:

The code counts and prints the occurrences of non-English words found in the extracted text.
It maintains a dictionary (non_english_word_counts) to keep track of non-English words and their counts.
The code then prints the non-English word count along with the word and its frequency.

Overall, this code can be used to extract specific content from a PDF file, validate the extracted words as English or non-English, and count the occurrences of non-English words in the extracted text. It's a useful tool for text analysis and processing tasks on PDF documents.
