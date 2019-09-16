# PatentPhraseEmbedding

The idea behind this phrase embedding is that we want to have different vectors for different senses. The straightforward solution is to just have two inputs for "oil", for example, "oil_o" and "oil_m".  We actually go beyond a single word embedding to do a better task of modelling complicated concepts. For instance, there is no individual usage of the term "oil" when refers to the concept "vehicle oil", or "vegetable oil", because they have different meaning.
Therefore we applied sophisticated NLP tasks to extract the important patent terms and phrases, and then each phrase is merged into a single token, so that it will be represented by a single vector. 

The model is trained on more than 13 millions patent sentences that are extracted from 5,000,000 patent documents.

**Model Training**  

We used the Word2vec implementation in Gensim (https:// radimrehurek.com/gensim/) with a few modifications. We found that skip-gram
with negative sampling loss (n = 15) performed best.  We used 100-dimensional embeddings, a learning rate of 0.01 decreasing to 0.0001 in 30 epochs, window set to 10, and a minimum word/phrase count set to 5.


The Embeddings model is availabel on Kaggle https://www.kaggle.com/darshmso/w2vec-patent-domain 

Examples of Word/Phrase Embedding: 
![arch_0000](https://github.com/sofean-mso/PatentPhraseEmbedding/blob/master/phraseEmbbs.png)



Another Examples:


![arch_0000](https://github.com/sofean-mso/PatentPhraseEmbedding/blob/master/phraseEmbb_auto_driving_und_quNTUM.png)



**References**                                                                                                             
*Mustafa Sofean, Ahmad Alrifai. Deep Learning Services for Patents. 1st Workshop on Patent Text Mining and Semantic Technologies. PatentSemTech 2019*
