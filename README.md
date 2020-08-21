# wink-eng-lite-model
**English lite language model for winkNLP**

[<img align="right" src="https://decisively.github.io/wink-logos/logo-title.png" width="100px" >](https://winkjs.org/)
This is a pre-trained English language model for the winkjs NLP package — [winkNLP](https://winkjs.org/wink-nlp/). The lite model package has a size of under 825KB, which expands to about 2.4MB after installation. It is an open-source language model, released under the MIT license.

It contains models for the following NLP tasks:

1. Tokenization
2. Token's Feature Extraction
3. Sentence Boundary Detection
4. Negation Handling
5. POS tagging
6. Automatic mapping of British spellings to American
7. Named Entity Recognition
8. Sentiment Analysis
9. Custom Entities Definition
10. *Lemmatization (upcoming)*



## Getting Started

### Installation
The model must be installed along with the [wink-nlp](https://winkjs.org/wink-nlp/):

```sh
# Install wink-nlp
npm install wink-nlp --save
# Install wink-eng-lite-model
node -e "require( 'wink-nlp/models/install' )" wink-eng-lite-model
```

### Example
We start by requiring the **wink-nlp** package and the **wink-eng-lite-model**. Then we instantiate wink-nlp using the language model:

```javascript
// Load "wink-nlp" package.
const winkNLP = require('wink-nlp');
// Load english language model — light version.
const model = require('wink-eng-lite-model');
// Instantiate wink-nlp.
const nlp = winkNLP(model);

// Code for Hello World!
var text = 'Hello   World!';
var doc = nlp.readDoc(text);
console.log(doc.out());
// -> Hello   World!
```

### Documentation
Learn how to use this model with winkNLP from the following resources:
- [Overview](https://winkjs.org/wink-nlp/) — introduction to winkNLP.
- [Concepts](https://winkjs.org/wink-nlp/getting-started.html) — everything you need to know to get started.
- [API Reference](https://winkjs.org/wink-nlp/read-doc.html) — explains usage of APIs with examples.
- [Release history](https://github.com/winkjs/wink-eng-lite-model/releases) — version history along with the details of breaking changes, if any.

## About model
### Performance
The [winkNLP](https://winkjs.org/wink-nlp/) processes raw text at **>600,000 tokens per second** with this model, when [benchmarked](https://github.com/bestiejs/benchmark.js) using "Ch 13 of Ulysses by James Joyce" on a 2.2 GHz Intel Core i7 machine with 16GB RAM. The benchmark covered the entire NLP pipeline — tokenization, sentence boundary detection, negation handling, sentiment analysis, part-of-speech tagging, and named entity extraction.

### Tokenization
While it is trained to process English language text, it can tokenize text containing other languages such as Hindi, French and German. Such tokens are tagged as **X** (foreign word) during pos tagging.

### POS Tagging
The model follows the [Universal POS tags](https://universaldependencies.org/u/pos/) standards. It delivers an accuracy of **~94.7%** on a subset of WSJ corpus — this includes *tokenization of raw text prior to pos tagging*.

### Named Entity Recognition (NER)
The model is trained to detect **CARDINAL**, **DATE**, **DURATION**,  **EMAIL**, **EMOJI**, **EMOTICON**, **HASHTAG**, **MENTION**, **MONEY**, **ORDINAL**, **PERCENT**, **TIME**, and **URL**.

### Sentiment Analysis
It delivers a [f-score](https://en.wikipedia.org/wiki/F1_score) of **~84.5%**, when validated using Amazon Product Review [Sentiment Labelled Sentences Data Set](https://archive.ics.uci.edu/ml/machine-learning-databases/00331/) at [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php).

### Storage Structure
The model is contained in the standard [NPM tarball](https://docs.npmjs.com/cli-commands/pack.html) format. You can find it under the latest [release](https://github.com/winkjs/wink-eng-lite-model/releases). The model is stored in form of trained data in JSON and binary formats. Apart from the data, there is a tiny fraction of JS glue code, which is primarily used during model loading.


## Need Help?
If you spot a bug and the same has not yet been reported, raise a new [issue](https://github.com/winkjs/wink-eng-lite-model/issues).

## About wink
[Wink](https://winkjs.org/) is a family of open source packages for **Natural Language Processing**, **Machine Learning** and **Statistical Analysis** in NodeJS. The code is **thoroughly documented** for easy human comprehension and has a **test coverage of ~100%** for reliability to build production grade solutions.


## Copyright & License
The **wink-eng-lite-model** is copyright 2020 of [GRAYPE Systems Private Limited](https://graype.in/).

It is licensed under the terms of the MIT License.

