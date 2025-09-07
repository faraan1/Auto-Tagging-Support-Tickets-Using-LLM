# Automated Support Ticket Tagging with LLMs
This project demonstrates how to use a large language model (LLM) for the automated classification of support tickets. It compares the performance of zero-shot and few-shot prompting techniques to tag incoming tickets with a predefined set of labels.

The primary model used in this demonstration is `google/flan-t5-large`. The script evaluates the model's ability to accurately classify tickets based on a simulated dataset.

## How It Works
The script operates in two main modes:
1. Zero-Shot Classification: The model is given a support ticket and a list of all possible tags. It must classify the ticket based on its pre-existing knowledge without any examples.
2. Few-Shot Classification: In addition to the list of tags, the model is provided with a few examples of tickets and their correct tags. This helps the model better understand the task and context, often leading to improved accuracy.

The script then compares the performance of both methods to determine which approach yields better results.

## Key Features
- Zero-shot and few-shot prompting: An easy-to-understand implementation of both prompting strategies.
- Performance Evaluation: Calculates and displays the top-3 accuracy for both zero-shot and few-shot methods on a given dataset.
- Hugging Face Integration: Uses the `transformers` library to seamlessly load and use the `google/flan-t5-large model`.
- Extensible: The simulated dataset and predefined tags can be easily replaced with your own data to test the model on real-world scenarios.

## Getting Started

## Prerequisites
- Python 3.x
- `torch`
- `transformers`
- `scikit-learn`

## Future Improvements
The current implementation does not include fine-tuning. For a production-ready solution, fine-tuning a smaller model on your specific dataset is highly recommended. The notebook provides a placeholder section with a link to the Hugging Face documentation to guide you on this process.
