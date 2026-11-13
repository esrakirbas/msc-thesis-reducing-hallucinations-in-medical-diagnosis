## Experiment 01 (November 13, 2026)

### Objective

I completed my first small-scale experiment using Qwen2.5-3B-Instruct and four manually selected questions from the MedQA dataset.
For grounding contexts, I used ChatGPT to help identify relevant passages from the medical textbooks included in MedQA.
The main objectives of this experiment were to become familiar with the development environment and tools, including Google Colab, Hugging Face, and GitHub, by building and running a complete experimental pipeline, and to gain a general understanding of how a context grounding pipeline works before moving to a more systematic experiment with larger benchmarks and corpora.

### Project Files

All files related to this experiment are stored in the `experiments/experiment01_medqa_manual_grounding/` folder in my GitHub repository. All .ipynb files are Google Colab notebooks.

| File | Description |
|---|---|
| [`Medical_Grounding_001_Data_Preparation_...ipynb`](Medical_Grounding_001_Data_Preparation_questions_and_corpus_from_MedQA.ipynb) | used to select MedQA questions, explore the textbook corpus, and prepare grounding contexts. |
| [`Medical_Grounding_002_Experiment1_...ipynb`](Medical_Grounding_002_Experiment1_MedQA_Manual_Grounding_with_QWEN.ipynb) | main experiment notebook containing Qwen model loading, baseline and grounded inference, and result comparison. |
| [`experiment01_questions_and_corpus.json`](experiment01_questions_and_corpus.json) | contains prepared data : four questions, answer options, reference answers, and grounding contexts. |
| [`grounding_contexts.txt`](grounding_contexts.txt) | Text file containing the manually selected textbook passages used for grounding. USed temporarily to prepare the data.|

The notebooks contain the implementation details and generated outputs, while this report documents the experiment's objectives, setup, results, and observations.

### Experimental Setup
I compared two approaches:
+ **Baseline:** The model answered questions without additional context.
+ **Context Grounding:** The model received manually selected passages from Harrison's medical textbook and was instructed to provide supporting quotations.

### Results:
+ **Baseline:** 1/4 correct answers (25%)
+ **Context Grounding:** 1/4 correct answers (25%)
Both approaches produced the same accuracy, although the selected answers differed for one question.

### Observations and Limitations:
Since the experiment includes only four questions, the results are not sufficient for general conclusions. However, this initial experiment showed some limitations of manual context selection and direct citation anchoring.
+ In the grounded experiment, the model sometimes provided quotations that did not support its answers
+ or quoted from the question instead of the textbook context. 

### Next steps: 
I will explore suitable medical benchmarks with supporting evidence and develop a more systematic grounding approach.
