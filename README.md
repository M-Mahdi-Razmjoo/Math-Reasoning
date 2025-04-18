# Math Reasoning with Mistral-7B-Instruct

This project evaluates the mathematical reasoning capabilities of the Mistral-7B-Instruct-v0.3 model on the GSM8K dataset using various prompting techniques. The goal is to assess how different prompting strategies impact the model's performance in solving grade-school-level math word problems.

## Project Overview

The notebook (`math reasoning.ipynb`) implements and compares multiple prompting methods to solve math problems from the GSM8K dataset. The methods include:

- **Direct Prompting**: Directly asking the model to provide answers with varying levels of reasoning (concise, step-by-step, brief final answer, detailed reasoning).
- **Zero-shot Prompting**: Encouraging the model to reason step-by-step without prior examples.
- **Few-shot Prompting**: Providing correct or incorrect example problems (shots) to guide the model.
- **Self-Consistency**: Generating multiple answers for each question and selecting the most frequent one.
- **Verbalized Confidence**: Generating multiple answers and selecting the one with the highest self-reported confidence score.
- **Subquestion Prompting**: Breaking down complex questions into simpler subquestions and solving them step-by-step.

The project uses the Hugging Face Transformers library to load the Mistral-7B-Instruct model and processes a subset of the GSM8K test set (default: 50 samples).
