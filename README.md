# Knowlets: A Vector Database & Network Visualization Toolkit

## Overview
Knowlets are designed as self-contained network visualizations and knowledge containers, capable of building a hierarchical structure of interconnected knowledge. Each Knowlet contains data and references to other Knowlets, allowing for complex data representations and analysis.

### Features
- **Hierarchical Knowledge Structure:** Build complex knowledge structures with parent and child Knowlets.
- **Data Association:** Associate data with each Knowlet for comprehensive knowledge representation.
- **Interactive Visualization:** Visualize Knowlet structures using network graphs.
- **Advanced Analysis Tools:** Perform topic modeling, sentiment analysis, and more.

## Major Updates

### Transition to Direct GPT Queries
- **Previously:** Utilized Langchain for response generation.
- **Now:** Directly queries GPT using OpenAI's Chat Completion API, specifically GPT-3.5 Turbo.

### Implementing Non-GPT Based LLM Parameters
- **Topic Modeling:** Uses Latent Dirichlet Allocation (LDA) for topic analysis, optimizing topic numbers and identifying key words.
- **Sentiment Analysis:** Employs nltk.sentiment.vader for sentiment scoring in Knowlet data.
- **Preprocessing:** Includes tokenization, lemmatization, stop word removal, etc., using libraries like nltk, gensim, and sklearn.

### Additional Features
- **Visualizing Knowlet Structure:** Network visualization using Pyvis.
- **Hierarchy Splitting:** Utilizes TF-IDF, cosine similarity, and Agglomerative Clustering for text similarity-based splitting, with dendrogram visualizations.
- **Autonomous Splitting:** Splits Knowlets using GPT-3.5 Turbo responses or non-GPT based topic modeling.
- **Parsing JSON Responses:** Converts JSON-formatted strings into Python dictionaries.

## Project Workflow
1. **Load Corpus:** Multiple text-based documents.
2. **Topic Identification and Sentiment Analysis:** Autonomous analysis using GPT or non-GPT methods.
3. **Splitting and Summarization:** Dividing Knowlets into relevant topics with concise summaries.
4. **Visualization:** Network graph to identify common topics and visualize sentiment.
5. **Bug Note:** Currently addressing a visualization bug related to the "__str__" function in Knowlets.

## Visualizations
- [GPT-Based Visualization](http://niksrid.me/knowlets-gpt-2.html)
- [GPT-2 Based Visualization](http://niksrid.me/knowlets-gpt.html)

## Future Directions
- **Querying Knowlets:** Implement complex queries for data retrieval.
- **Dynamic Networks:** Enable Knowlets to integrate into various networks, enhancing modularity.
- **Library Development Goals:**
  - Consume and preprocess a corpus.
  - Autonomously split the network with search and filter functionalities.
  - Cache GPT-3.5 responses for efficiency and cost reduction.
  - Explore dynamic and interchangeable network capabilities.

### Notes on Implementation
- **Open Source LLM Usage:** Initially planned, but switched to GPT-3.5 Turbo for better results.
- **Non-GPT Based Modeling:** Ongoing development for enhanced statistical and deep learning models.

## Conclusion
This project exemplifies the potential of Knowlets as dynamic knowledge containers, capable of autonomously processing and integrating data within diverse networks, adhering to the core principles outlined in the initial paper.
