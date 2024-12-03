## Rag Evaluation

As we know Rag has two Parts 
1. Retrieval
2. Generation.

Now specifically for retrieval we use precision , recall , f1 score and specifically for generation we use bleu/rough score as well as we can do Human evaluation too.

Now in this code i have used RAGAS that is a framework implemented for Rag evaluation. I will explain the meaning of those metrics and their usage
1. Context Precision -> It checks whatever documents have retrieved how many of them are relevant
2. Context Recall -> It checks how much necessary documents have been retrieved , if any missing documents exists or not
3. Faithfullness -> It checks how much  generated answer is relevant with the retrieved documents
4. Answer Relevancy -> It checks how much generated answer is relevant with the user query

We need to see precision one when our llm is retrieving many documents but only few of them are used to answer the query of the user. For the real time example if I say then in my notebook you can see context precsion came nan that means it probably happened because my all contexts are same and i used very small txt file to get this questions and answers.

We need to see recall one when our llm is retrieving many documents but few of them are missing anc causing incomplete or maybe wrong answer

We need to use Faithfullness when we need to check the genarated answers are matching with the retrieved documents or not, just we want to ignore hallucinated answers. we will some factual checkup with relevant documents that we will have

We need to use answer relevancy when we need to check generated answer directly matching with the user query or generated answer is directing somewhere else instead of the user query's direction.
