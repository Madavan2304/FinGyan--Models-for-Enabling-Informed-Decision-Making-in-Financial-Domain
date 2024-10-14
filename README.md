# FinGyan: Models for Enabling Informed Decision-Making in Financial Domain

**Overview**

The FinGyan project leverages advanced natural language processing (NLP) and reinforcement learning (RL) techniques to develop models that provide insights and decision-making support in the financial domain. The project comprises four main components: Financial Named Entity Recognition (FinNER), Financial Summarization (FinSUM), Financial Question Answering (FinQA), and Reinforcement Learning for Portfolio Optimization (RLOpt). These models are designed to assist analysts, investors, and financial institutions in extracting, summarizing, understanding, and acting on financial information effectively.

**Key Objectives**

* Identify Key Financial Entities: Use NLP techniques to accurately recognize and classify financial entities such as companies, monetary amounts, and stock symbols in large datasets.
* Summarize Financial Documents: Provide concise and accurate summaries of lengthy financial reports to support faster and more informed decision-making.
* Answer Financial Queries: Build models capable of answering complex financial questions, improving user interaction and understanding of financial concepts.
* Optimize Investment Portfolios: Develop RL-based models to recommend optimal asset allocations for portfolio management.
  
**Model Development**

**1. FinNER (Financial Named Entity Recognition):**
* Dataset Preparation: Load and preprocess financial NER datasets like tner/fin for fine-tuning. Tokens are concatenated to form text sequences suitable for training.
* Fine-Tuning: Leverage transformer models (e.g., tner/roberta-large-fin) with PEFT (Parameter Efficient Fine-Tuning) and utilize advanced features like mixed precision and quantization to optimize model training.
* Visualization: Implement the use of spacy and displacy for visualizing the named entities detected in the financial text to ensure proper model performance and annotation accuracy.

**2. FinSUM (Financial Summarization):**
* **Data Preparation:** Use large financial text datasets for summarization tasks. Tokenize and structure these using PegasusTokenizer for model compatibility.
* **Fine-Tuning Pegasus Model:** Customize the PegasusForConditionalGeneration model for financial summarization tasks, incorporating dropout for regularization and freezing encoder layers when needed to focus learning on specific parts of the model.
* **Inference & Summarization:** Implement a method for summarizing multi-line financial documents input by users, using the fine-tuned model for generating concise and relevant summaries.

**3. FinQA (Financial Question Answering):**
* Dataset Reformatting: Convert the dataset format to align with instruction-following large language models (LLMs), including defining human-assistant roles within the data entries.
* LLM Fine-Tuning: Employ an LLM like AdaptLLM/finance-chat with custom parameters for optimized training and inference efficiency. Incorporate techniques like prompt engineering for better model responses to financial queries.
* Response Generation: Utilize models such as vllm to generate detailed, contextually accurate answers to financial queries, using specific prompts for evaluating financial and investment concepts.

**4. RLOpt (Reinforcement Learning for Portfolio Optimization):**
* Environment Setup: Design a custom reinforcement learning environment using Gym for portfolio optimization, where action spaces correspond to asset allocation weights.
* Training an RL Model: Use algorithms like A2C with customized policy and optimizer configurations for training. Simulate real-world financial conditions with risk and volatility adjustments to enhance the model's decision-making ability.
* Optimal Portfolio Identification: Analyze the trained model's performance to derive optimal weights for a portfolio, calculate metrics such as portfolio return, risk, Sharpe ratio, and visualize these using a structured data analysis framework.


**Tools and Libraries**

* Jupyter Notebook & Kaggle: For development and documentation of code execution and results visualization.
* Pandas & NumPy: For data manipulation and numerical computations.
* Transformers: For model development and fine-tuning.
* Gym & Stable Baselines: For building and training reinforcement learning models for portfolio optimization.
* Spacy & Displacy: For visualizing named entities in financial text.

By following this structured approach and utilizing state-of-the-art tools and techniques, the FinGyan project aims to deliver comprehensive and actionable financial models that provide critical insights and support strategic decision-making in the financial sector.
