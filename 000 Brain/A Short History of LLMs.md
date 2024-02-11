---
Created On: 2023-10-30, 10:06
Unique ID: 202310301006
---


**Status:** #review 

**Tags:** #SoftwareCards 

# A Short History of LLMs

#### How do LLMs work?
?
They parse human text into tokens and then produce vectors of associated and unassociated words for each token. These vectors will contain hundreds of thousands of entries. Similar words will have similar vectors, i.e., `sea` and `ocean`.
<!--SR:!2024-03-17,88,270-->


#### What advancement led to modern (circa 2023) LLMs?
?
Before 2017, LLMs used RNNs or recurrent neural networks, which scanned each words in a sentence sequentially. In 2017, researchers at google published the transformer model. The transformer model processes entire blocks at once - sentences, paragraphs, articles, etc... analyzing all parts, not just individual tokens.
<!--SR:!2024-02-12,2,190-->

#### In relation to LMMs, what is "self-attention"?
?
Self-attention looks at each token in a body of text and decides which other tokens are most important to understand the tokens means.
![[Screenshot 2023-10-30 at 10.12.01 AM.png|400]]
<!--SR:!2024-05-02,118,270-->


#### In relation to LLMs, what is greedy vs beam search?
?
Greedy search is filling in the next token based on the probability of individual tokens. Beam search calculates the probability of a sequence of words, including the probabilities of all the words in the sequence. 
<!--SR:!2024-03-05,76,250-->


---
# References
[A fun website Patrick sent C4B Therapy](https://ig.ft.com/generative-ai/)
[Google Research Paper](https://blog.research.google/2017/08/transformer-novel-neural-network.html)

