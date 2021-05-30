# Latent-Dirichlet-Allocation-LDA-

What is LDA?

Latent Dirichlet allocation (LDA) is a topic model that generates topics based on word frequency from a set of documents. LDA is particularly useful for finding reasonably accurate mixtures of topics within a given document set.

LDA walkthrough

This walkthrough goes through the process of generating an LDA model with a highly simplified document set. This is not an exhaustive explanation of LDA. The goal of this walkthrough is to guide users through key steps in preparing their data and providing example output.

Packages required

This walkthrough uses the following Python packages:

NLTK, a natural language toolkit for Python. A useful package for any natural language processing.

For Mac/Unix with pip: $ sudo pip install -U nltk.

stop_words, a Python package containing stop words.

For Mac/Unix with pip: $ sudo pip install stop-words.

gensim, a topic modeling package containing our LDA model.

For Mac/Unix with pip: $ sudo pip install gensim.

So what does LDA actually do?

This explanation is a little lengthy, but useful for understanding the model we worked so hard to generate.

LDA assumes documents are produced from a mixture of topics. Those topics then generate words based on their probability distribution, like the ones in our walkthrough model. In other words, LDA assumes a document is made from the following steps:

Determine the number of words in a document. Let’s say our document has 6 words. Determine the mixture of topics in that document. For example, the document might contain 1/2 the topic “health” and 1/2 the topic “vegetables.” Using each topic’s multinomial distribution, output words to fill the document’s word slots. In our example, the “health” topic is 1/2 our document, or 3 words. The “health” topic might have the word “diet” at 20% probability or “exercise” at 15%, so it will fill the document word slots based on those probabilities. Given this assumption of how documents are created, LDA backtracks and tries to figure out what topics would create those documents in the first place.
