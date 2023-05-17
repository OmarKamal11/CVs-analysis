# Resumes_Analysis
This project focuses on text processing, analysis, and matching job skills. It starts by installing and managing the necessary libraries such as Spacy, nltk, pyresparser, ftfy, and python-docx. These libraries provide functionality for natural language processing (NLP), resume parsing, and document manipulation.

Then defines utility functions for text processing and analysis. These functions handle tasks like tokenization, stemming, and n-gram generation. Tokenization splits text into individual words or tokens, while stemming reduces words to their root form for simplified comparison. N-grams are subsequences of words, which can be useful for capturing contextual information.

Once the skills data is obtained using the ResumeParser class from pyresparser and the Document class from python-docx , it undergoes further processing and transformation. The code applies the defined text processing functions to clean and normalize the skills data, removing stopwords and applying stemming to reduce words to their base forms. This step helps in standardizing the representation of skills for subsequent analysis and comparison.

Next, the TfidfVectorizer class from sklearn compute the TF-IDF (Term Frequency-Inverse Document Frequency) representation of the skills data. TF-IDF is a numerical statistic that reflects the importance of a word within a collection of documents. It assigns higher weights to words that appear frequently in a particular document but rarely in other documents.

The TF-IDF representation is then used to compute the cosine similarity between the skills data and a dataset of job descriptions. Cosine similarity measures the similarity between two vectors and can be used to find the most similar job descriptions for a given set of skills. The NearestNeighbors class from sklearn find the nearest neighbors based on cosine similarity.

Finally, the script presents the top matching jobs based on the computed similarity scores. It sorts the job descriptions by match confidence and presents relevant information such as job title, company, location, and match confidence. The resulting list of job descriptions is sorted in descending order of match confidence, allowing users to identify potential job opportunities that closely align with their skills.

In summary, this project combines NLP techniques, resume parsing, and similarity matching to help users find job opportunities that match their skills.
