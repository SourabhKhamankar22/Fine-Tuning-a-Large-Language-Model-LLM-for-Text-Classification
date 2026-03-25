# Fine-Tuning a Large Language Model (LLM) for Text Classification

## Overview
This project demonstrates the application of Transfer Learning to fine-tune a pre-trained Large Language Model (LLM) for a specific Natural Language Processing (NLP) task. Specifically, it fine-tunes the `distilbert-base-uncased` model to perform binary sentiment analysis (Positive/Negative) on the IMDb Movie Review Dataset.

## Project Details
* **Core Focus:** Large Language Models (LLM), Transfer Learning, NLP Pipelines
* **Model Used:** DistilBERT (`distilbert-base-uncased`)
* **Dataset:** IMDb Movie Review Dataset (25,000 training samples, 25,000 testing samples)
* **Task:** Binary Text Classification (Sentiment Analysis)

## Performance & Results
After fine-tuning the model for 2 epochs, it successfully learned to classify movie reviews with high precision:
* **Final Accuracy:** 92.32%
* **Final F1-Score:** 92.14%

The model successfully leverages Transfer Learning—taking a model that already understands general English grammar and syntax and adjusting its final layers specifically for sentiment detection, saving immense computational resources compared to training from scratch.

## Prerequisites & Environment Setup
To replicate this project locally, it is recommended to use Anaconda to manage the dependencies, especially for GPU acceleration.

**1. Create the Conda Environment:**
```bash
conda create -n llm_finetuning python=3.10 -y
conda activate llm_finetuning
```
**2. Install PyTorch (with CUDA support for NVIDIA GPUs):**
```
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia -y
```
**3. Install Required NLP Libraries:**
```
pip install transformers datasets evaluate scikit-learn jupyter accelerate
```
**4. Resolve Dependency Conflicts (If necessary):**
If you encounter a sympy version conflict with PyTorch, run:
```
pip install sympy==1.13.1
```
**Usage**
1. Clone this repository to your local machine.
2. Ensure your llm_finetuning conda environment is activated.
3. Launch Jupyter Notebook or open the project in VS Code:
```
jupyter notebook
```
4. Open major.ipynb and select the llm_finetuning Python kernel.
5. Run the cells sequentially to download the data, train the model, and evaluate the results.

**Inference on Custom Data**
The notebook includes a built-in function to test the model on unseen data. You can pass any custom string to the `predict_sentiment()` function at the end of the notebook to get a Positive or Negative classification.
Example:
```
text = "The cinematography was absolutely breathtaking, but the plot was a bit slow."
# Output: Positive
```