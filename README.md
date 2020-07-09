# wink-eng-lite-model
English lite language model for wink-nlp.

[<img align="right" src="https://decisively.github.io/wink-logos/logo-title.png" width="100px" >](http://wink.org.in/)
This is a pre-trained English language model for the winkjs NLP package — [wink-nlp](https://winkjs.org/wink-nlp/). The lite model package has a size of under 800KB, which expands to about 2.4MB after installation. It contains models for the following NLP tasks:

1. Tokenization
2. Token's Feature Extraction
3. Sentence Boundary Detection
4. Negation Handling
5. POS tagging
6. Lemmatization (upcoming)
7. Named Entity Recognition
8. Sentiment Analysis
9. Custom Entities Definition



### Getting Started

#### Installation
The model must be installed along with the [wink-nlp](https://winkjs.org/wink-nlp/):

```sh
# Install wink-nlp
npm install wink-nlp --save
# Install wink-eng-lite-model
npm install https://github.com/winkjs/wink-eng-lite-model/releases/download/0.2.0/wink-eng-lite-model-0.2.0.tgz --save
```

#### Example
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


#### Documentation
Check out the wink-nlp's [concepts](https://winkjs.org/wink-nlp/getting-started.html) and  [API reference](https://winkjs.org/wink-nlp/read-doc.html) to learn more about the package.

### Need Help?
If you spot a bug and the same has not yet been reported, raise a new [issue](https://github.com/winkjs/wink-eng-lite-model/issues).

### About wink
[Wink](http://winkjs.org/) is a family of open source packages for **Natural Language Processing**, **Machine Learning** and **Statistical Analysis** in NodeJS. The code is **thoroughly documented** for easy human comprehension and has a **test coverage of ~100%** for reliability to build production grade solutions.


### Copyright & License
The **wink-eng-lite-model** is copyright 2020 of [GRAYPE Systems Private Limited](http://graype.in/).

It is licensed under the terms of the MIT License.

