# Academic Papers Retrieval System
This is an information retrieval system for academic papers that has advanced features and can retrieve and recommend papers to the user using Machine Learning methods. It is implemented in Python and required libraries and packages are listed at the beginning of every section. It consists of three phases which I will elaborate on:
## Phase 1: Classic information retrieval system
In this phase, I utilized a dataset of academic papers from [Semantic Scholar](https://www.semanticscholar.org/), which included paperID, title, and abstract information. Initially, I applied preprocessing techniques using [NLTK](https://www.nltk.org/) and [SpaCy](https://spacy.io/) to clean and prepare the data for analysis.

Next, I constructed a positional index for the documents, allowing for efficient retrieval of information. To optimize storage, I implemented index compression methods like gamma coding and variable-byte encoding, significantly reducing the size of the index file.

Additionally, I integrated spell correction into the system, enhancing the accuracy of search queries. I implemented various TF-IDF vector space methods, along with the Okapi BM25 method, to analyze the document collections effectively and give score to different documents.

In the evaluation phase, I calculated different metrics such as precision, recall, and F1 score to assess the performance of the implemented methods. By comparing the results of these various techniques, I gained valuable insights into their effectiveness and applicability for the information retrieval system.
## Phase 2: Adding Machine Learning methods to the system
In this phase, my main focus was on document classification and clustering using Machine Learning methods. Initially, I implemented a Naive Bayes classifier from scratch and evaluated its performance using advanced metrics such as the ROC curve and corresponding AUC scores.

Next, I moved towards document classification using neural networks. I utilized Fasttext to obtain embeddings for each document. Similarly, I calculated an embedding for the user's query. Subsequently, I built a classifier model using PyTorch and trained it with the input data. I thoroughly evaluated the model's performance using various metrics.

In the subsequent step, I explored document classification using language models. Leveraging the transformers library, I fine-tuned the pre-trained BERT model to construct my own model. I subjected this model to a comprehensive evaluation.

Lastly, I introduced document clustering into my system. To achieve this, I first obtained document embeddings and utilized [Hugging Face](https://huggingface.co/) models based on transformers, specifically BERT. I then implemented the k-means algorithm from scratch, calculating the Silhouette score for different values of k. Additionally, I explored hierarchical clustering using the [SciPy](https://scipy.org/) library.
## Phase 3: Adding web crawler to the system and build a personalized search engine using recommender systems
In this phase, I incorporated a web crawler to gather paper information from Semantic Scholar, utilizing [Selenium](https://www.selenium.dev/documentation/webdriver/) for web automation and then parsing the collected data using [Beautiful Soup](https://pypi.org/project/beautifulsoup4/#:~:text=Beautiful%20Soup%20is%20a%20library,and%20modifying%20the%20parse%20tree.). Subsequently, I developed a personalized PageRank algorithm that takes into account user preferences, enhancing the relevance of the retrieved papers.

Following this, I implemented the HITS algorithm to rank the authors of the papers, providing insights into their influence and contribution within the academic community.

Finally, I created a recommender system, employing both collaborative filtering and content-based approaches. I thoroughly compared the outcomes of these methods, evaluating their effectiveness and suitability for the information retrieval system.
