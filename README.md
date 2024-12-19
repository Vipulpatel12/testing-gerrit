Sure, here is the code:

```python
def check_system(system):
    import re
    from nltk.corpus import stopwords
    from sklearn.feature_extraction.text import CountVectorizer
    from sklearn.metrics.pairwise import cosine_similarity
    stop_words = set(stopwords.words('english'))
    
    def preprocess(input_string):
        return ' '.join([word for word in input_string.split() if word not in stop_words])
    
    system['text'] = system['title'] + " " + system['description']
    system['text'] = [preprocess(review) for review in system['text']]
    vectorizer = CountVectorizer().fit_transform(system['text'])
    vectors = vectorizer.toarray()
    
    csim_matrix = cosine_similarity(vectors, vectors)
    system['csim_matrix'] = csim_matrix
```
