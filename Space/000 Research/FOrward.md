##### Challenge naive RAG
- Bad retrieval
	- Low precision
	- low recall: lack enough context for LLM to synthesize the answer
	- Outdated info: data is redundant or out of date
- Bad response
	- Hallucination: Model makes up an answer that isn't in the context
	- Irrelevance: answer that doesn't answer the question
	- Toxicity/Bias: answer that harmful or offensive
##### RAG System
Doc -> Chunks -> vector database -> chunks -> LLM
Data -> embeddings -> retrieval -> synthesis

