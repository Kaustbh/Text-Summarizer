# Text-Summarizer


 
## Table of Contents

- [Introduction](#introduction)
- [Dataset Used](#dataset-used)
- [Model Used](#model-used)
- [Workflow of Project](#workflow-of-project)
- [Pipeline](#pipeline)
  - [Data Ingestion](#data-ingestion)
  - [Data Validation](#data-validation)
  - [Data Transformation](#data-transformation)
  - [Model Training](#model-training)
  - [Model Evaluation](#model-evaluation)
- [Running the Project](#running-the-project)
- [Contributing](#contributing)
- [License](#license)

## Introduction

### Text-Summarizer:

A powerful and efficient text summarization tool designed to condense large bodies of text into concise summaries, preserving key information and insights.

## Dataset Used

- #### Samsum Dataset 

The SAMSum dataset contains about 16k messenger-like conversations with summaries.
You can get the dataset from Hugging Face , https://huggingface.co/datasets/samsum?row=10 

## Model Used

- #### Google Pegasus Model

The project utilizes the Google Pegasus model, a state-of-the-art transformer-based model for text generation tasks, including summarization. Developed by Google Research, Pegasus stands for Pre-training with Extracted Gap-sentences for Abstractive SUmmarization of Texts. It is designed to generate abstractive summaries by learning to predict masked tokens in a text, making it highly effective for tasks requiring understanding and summarizing long texts.

 ## Workflow of Project

1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. Update the components
6. Update the Pipeline
7. Update the main.py
8. Update the app.py

## Pipeline

- #### Data Ingestion

The data ingestion phase involves downloading the dataset from hugging face and unzipping it into a designated directory. 

- #### Data Validation

After ingestion, the dataset undergoes validation to ensure all required files are present and correctly formatted. This process checks for the presence of 'train', 'test', and 'validation' directories and logs the status.

- #### Data Transformation

In the data transformation phase, the dataset is further processed to prepare it for model training. This includes tokenization using the Google Pegasus tokenizer (`google/pegasus-cnn_dailymail`).

- #### Model Training

The model training phase involves training the Google Pegasus model on the transformed dataset.

- #### Model Evaluation

Finally, the trained model is evaluated on the same dataset used for training.

## Running the Project

To clone and run the project, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/Kaustbh/Text-Summarizer.git
```

2. Navigate to the project directory:

```bash
cd Text-Summarizer
```

3. Create a Python virtual environment (optional but recommended):

```bash
python -m venv venv
```

4. Install the required packages:

```bash
pip install -r requirements.txt
```

5. Run the Flask app:

```bash
flask --app app run --debug
```

## Contributing

Contributions to this project are welcome. If you encounter any issues or have suggestions for improvements, please submit a pull request or open an issue on the GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to customize this README file to include specific details about your project, such as how to extend the functionality, examples of usage, or any additional acknowledgments.