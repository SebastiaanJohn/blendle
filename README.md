# Blendle - Topic-based Event Timeline

For the course: Leren en Beslissen at the University of Amsterdam.

In Blendle’s words: “News develops. Real-world events rarely stand by themselves.” A great timeline helps the reader understand how news stories develop and how events are related. Yet, creating a timeline by hand takes a lot of labor hours which results in high personnel costs. Therefore, automating this process would be of high value for Blendle. Their challenge consisted of extracting key news events from a large dataset of articles for the following topics: The coronavirus, Black Lives Matter, Brexit, Formula 1, and putting these in a comprehensive timeline. Finally, the solution should generalize beyond this list of topics.

The dataset consisted of 1 million Dutch news articles and around 400k English articles from 2019 to 2020 in JSON format.

There is one solution for Dutch- and one for English-articles. The Dutch solution uses a Top2Vec model while the English model uses BERTopic. Both methods share the same general structure: first, the documents are embedded. Next, the embeddings pass through a UMAP dimensionality reduction method. Then, HDBSCAN clusters the embeddings. Finally, the BERT extractive summariser makes a summary for each article. 
