# Plagiarism Detection with 3 Machine Learning models

This repository contains code and associated files for deploying a plagiarism detector using [Amazon SageMaker](https://aws.amazon.com/sagemaker/), [Sklearn](https://scikit-learn.org/stable/) and [PyTorch](https://pytorch.org).

## Project Overview

This project is about to build a plagiarism detector that examines a text file and performs binary classification; labeling that file as either **plagiarized** or **not**, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

This project will be broken down into three main notebooks:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.

**Notebook 2: Feature Engineering**

* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**

* Upload train/test feature data to S3.
* Define a binary classification model and a training script in 3 versions: 
  * XGBoost build-in Amazon SageMager impelmentation - 92% of accuracy,
  * RandomForest Sklearn implementation - 96% of accuracy,
  * my Full Connected layers implementation using PyTorch - 100% of accuracy.
* Train your model and deploy it using SageMaker.

## Installation

You need [Amazon Sagemaker](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html) and a [Notebook instance](https://docs.aws.amazon.com/sagemaker/latest/dg/gs-setup-working-env.html) to run this code. While creating a Notebook instance you can add link to this [repository](https://github.com/karolcichosz/project-plagiarism-detection.git), so can can have this project placed in your Notebook instance. All step by step detailed instructions are provided in Jupiter Notebook files 1, 2 & 3.

## Licence

Copyright: [Karol Cichosz](https://www.linkedin.com/in/karolcichosz/): The content of this repository is licensed under [MIT licence](https://choosealicense.com/licenses/mit/).
