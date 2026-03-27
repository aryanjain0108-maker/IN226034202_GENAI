1. Difference between "Love" and "love" in NLP

In Natural Language Processing (NLP), "Love" and "love" are considered different tokens if the text is case-sensitive. This means the model treats them as separate words, even though they represent the same concept. "Love" is usually capitalized when it appears at the beginning of a sentence or as a proper noun, while "love" is used in general contexts.If case normalization (lowercasing) is not applied, it can increase the vocabulary size unnecessarily and create duplicate features, which reduces model efficiency. For example, a sentiment analysis model may treat "Love this movie" and "love this movie" differently, even though they have the same meaning.
Therefore, converting all text to lowercase during preprocessing ensures uniformity, reduces redundancy, and improves the performance of NLP models.

2. What happens if stopwords are not removed?

Stopwords are commonly used words such as "is", "the", "and", "in", which usually do not carry significant meaning in text analysis. If stopwords are not removed, they increase the size of the dataset and introduce noise, making it harder for models to focus on important words.This can lead to increased computational cost, slower processing time, and reduced model accuracy, especially in tasks like text classification or information retrieval. For example, in a sentence like "This is a very good product", words like "is" and "a" do not contribute much to understanding the sentiment.
However, in some cases, keeping stopwords may be useful depending on the application. Overall, not removing stopwords can negatively affect efficiency and model performance in many NLP tasks.

3. Two real-world scenarios where removing stopwords can be harmful

Removing stopwords is not always beneficial, as some stopwords carry important meaning in specific contexts.
1. Sentiment Analysis:
Words like "not", "no", and "never" are often considered stopwords but are crucial for understanding sentiment. For example, "This product is good" and "This product is not good" have opposite meanings. Removing "not" would lead to incorrect interpretation.
2. Question Answering Systems / Search Engines:
Stopwords such as "who", "what", "where", and "when" are essential for understanding user queries. For example, "Who invented the telephone?" loses its meaning if "who" is removed. This can result in irrelevant or incorrect answers.
Thus, blindly removing stopwords can lead to loss of important contextual information and degrade system performance.

4. Difference between Stemming and Lemmatization

Stemming and lemmatization are techniques used to reduce words to their base or root form, but they work differently.
Stemming is a simple and fast process that removes prefixes or suffixes from words without considering the context. For example, "running", "runner", and "runs" may all be reduced to "run". However, stemming can sometimes produce incorrect or non-dictionary words, such as "better" becoming "bet".
Lemmatization, on the other hand, is a more advanced technique that converts words into their base dictionary form (lemma) using linguistic rules and context. For example, "running" becomes "run" and "better" becomes "good". It produces more accurate and meaningful results but requires more computational resources.
In summary, stemming is faster but less accurate, while lemmatization is slower but more precise and context-aware.
