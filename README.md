# PatentPhraseEmbedding

The idea behind this phrase embedding is that we want to have different vectors for the different senses. The straightforward solution is to just have two inputs for "oil", for example, "oil_o" and "oil_m".  We go beyond a single word embedding to do a better task of modelling complicated concepts. For instance, there is no individual usage of the term "oil" when refers to the concept "vehicle oil", or "vegetable oil", because they have different meaning.
Therefore we applied sophisticated NLP tasks to extract the patent terms and phrases, and then each phrase is merged into a single token, so that it will be represented by a single vector. 

The model is trained on more than one billion words and phrases, and more than 13 millions patent sentences that are extracted from 5,000,000 patent documents.

Word/Phrase Embeddings: 
![arch_0000](https://github.com/sofean-mso/PatentPhraseEmbedding/blob/master/phraseEmbbs.png)

