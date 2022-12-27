---
layout: post
title: Working through the Textacy SVO
---

If you have landed here, then you have been intrigued by the possibility of handing over having [Textacy](https://textacy.readthedocs.io/en/latest/) do the work of delivering subject-verb-object triples out of your text data. It can be done, but there are some nuances to making things happen. 

One of the first issues I encountered was getting `ValueError`s for `nlp.maxlength` when using Textacy's built-in function, but if I used [spaCy](https://spacy.io/) to create a spaCy `doc` everything was fine:

```python
# Load the Space pipeline to be used
nlp = spacy.load('en_core_web_lg')

# Use the pipe method to feed documents 
docs = list(nlp.pipe(texts_f))

# Checking to see if things worked:
docs[0]._.preview
```
Please note that Textacy does have a `corpus` object. I have not used it yet, but it looks like you could simply feed it the list of spaCy docs. It allows you to bundle metadata with the texts -- I would like to see examples of how people are using it.

```python
corpus = textacy.Corpus("en_core_web_sm", data=docs)
```

Spacy has built-in PoS tagging, accessing it looks like this:

```python
for token in docs[0][0:5]:
    print (token, token.tag_, token.pos_) # spacy.explain(token.tag_)
```

```python
# If we want to see all the nouns used 
# as subjects in the test document:
subjects = [str(item[0]) for item in SVOs]
subjects_set = set(subjects)

print(f"There are {len(subjects_set)} unique subjects out of {len(subjects)}.")
print(subjects_set)
```

```python
# Get out just the first person singular triples:
for item in SVOs:
    if str(item[0]) == '[i]':
        print(item)
```

It looks like the verb "contents" -- the verb phrase -- contains more material than we want. If all we want is the very itself, we will need to target the last item in the verb list.

```python
for item in SVOs:
    if str(item[0]) == '[i]':
        print(item[1][-1])
```