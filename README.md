Vector Space Model (VSM) Search Engine
This project is an implementation of a Vector Space Model (VSM) search engine in Python, which uses TF-IDF (Term Frequency - Inverse Document Frequency) to rank documents based on their relevance to a given query.

Features
Indexing Documents: Text documents are processed to extract terms and build a dictionary of terms and their frequencies.
Cosine Similarity Ranking: Documents are ranked using cosine similarity based on the term weights from the query and documents.
TF-IDF Weighting: Both documents and queries are weighted by their term frequency (TF) and inverse document frequency (IDF).
Query Processing: The system processes queries and returns the top 10 most relevant documents based on their similarity to the query.
Interactive File Upload: Users can upload multiple .txt files and run queries on them using a widget interface.
Dependencies
The project requires the following Python libraries:

math: For logarithmic and square root calculations.
collections: For defaultdict and Counter to handle document frequencies and term counts.
ipywidgets: For creating an interactive file upload widget in Jupyter Notebooks.
IPython.display: To display the widget in Jupyter.
You can install any missing dependencies via pip:

bash
Copy code
pip install ipywidgets
How to Run
Set up Jupyter Notebook: Ensure you have Jupyter Notebook installed. If not, you can install it via:

bash
Copy code
pip install notebook
Upload the Documents:

Once the notebook is running, an interactive file upload widget will appear.
Upload the .txt files (documents) you wish to index and search.
Automatic Execution:

After uploading the files, the program will automatically index the documents and execute predefined queries.
The top 10 most relevant documents for each query will be printed along with their similarity scores.
Custom Query: You can modify the queries in the on_button_click function within the code.

Example Usage
Predefined Queries
Once the documents are uploaded, three sample queries are executed:

Query 1: "Developing your Zomato business account and profile is a great way to boost your restaurant’s online reputation"
Query 2: "Warwickshire, came from an ancient family and was the heiress to some land"
Query 3: "Hewlett-Packard (HP) was founded in 1939"
The system will print the top 10 most relevant documents for each query with their corresponding relevance scores.

Adding Custom Queries
To modify the queries, locate the following lines in the code and adjust the query text as needed:

python
Copy code
query1 = "Your custom query here"
File Structure
bash
Copy code
IR_Assingment2_VSM.ipynb     # Jupyter Notebook containing the VSM implementation
How the Code Works
Document Indexing:

The function index_documents reads and processes all uploaded .txt files, splitting them into terms and calculating term frequencies.
The dictionary keeps track of each term's document frequency (df) and the postings list containing document IDs and term frequencies.
Document Length Calculation:

The length of each document is calculated based on the term frequency (TF) and inverse document frequency (IDF) of terms in the document.
Query Processing:

The query is tokenized, and each term's TF and IDF are calculated, forming the query vector.
Document Ranking:

The system calculates cosine similarity between the query vector and each document vector, normalizing by document length.
Documents are sorted and ranked by similarity score, with the top 10 most relevant documents returned.
Acknowledgments
This project was built using Python and Jupyter Notebook to demonstrate a simple, yet effective, search engine using the Vector Space Model.