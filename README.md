# Reading Comprehension with BERT

This repository contains the code and documentation for a reading comprehension project using BERT. The goal of this project is to fine-tune a pre-trained BERT model for a reading comprehension task—reading a passage and selecting the correct answer from given choices.

---

## Project Overview

- **Task:**  
  The model reads a passage, processes a question about that passage, and selects the correct answer from three available choices. This task requires deep understanding of the context, details, and nuances in the text.

- **Model:**  
  - **BERT:**  
    BERT (Bidirectional Encoder Representations from Transformers) is leveraged as the core language model to understand context in both directions.  
  - **Fine-Tuning:**  
    A pre-trained BERT model is fine-tuned on the reading comprehension dataset. The project uses a tiny BERT model as a benchmark, with options to tune hyperparameters and experiment with more advanced models such as `bert-base-uncased` and `bert-large-uncased`.

- **Dataset:**   (https://drive.google.com/file/d/1LABaYT-2gWthtNnW7PKlG9pM8Mh3NvuA/view)
  - **Training Data:** `train_data.csv` with 8488 rows and 7 columns, including:
    - Question ID
    - Context (passage)
    - Question text
    - Three answer choices
    - Label indicating the correct answer (choice number)
  - **Test Data:** `test_data.csv` with 2122 rows and 7 columns (the label column is “Null”)

---

## Implementation Details

- **Data Processing:**  
  The notebook processes the CSV data, tokenizes the passages and questions, and prepares the dataset for model training.

- **Model Training:**  
  - The fine-tuning process runs for approximately 2 minutes for data processing and 2 minutes for training with the sample code.
  - Hyperparameters (e.g., learning rate, batch size, number of epochs) are tuned to optimize performance.
  - 
  ![image](https://github.com/user-attachments/assets/ffda38f2-eb5a-41cf-ab3b-3f7db7112eed)

- **Advanced Options:**  
  For more advanced experimentation, you can switch to larger pre-trained models such as `bert-base-uncased` or `bert-large-uncased` to potentially improve accuracy, keeping in mind the longer processing times required.

- **Output:**  
  - The final predictions on the test set are saved in a CSV file with two columns:
    - **id:** Row index
    - **label:** Predicted answer label (0, 1, or 2)

- **Evaluation:**  
  Model performance is measured by categorization accuracy—the higher the accuracy, the better the model’s understanding of the text.
  
![image](https://github.com/user-attachments/assets/ea08128e-de0b-4955-9b39-7822d9b49d48)

---

## Files Included

- **Jupyter Notebook:**  
  - `DL_Weeek10 (2).ipynb` – Contains the full implementation for data processing, model fine-tuning, and evaluation.
  
- **Datasets:**  
  - `train_data.csv`
  - `test_data.csv`
  - The output CSV file includes two columns: `id` and `label` for Kaggle submission.

---

## Conclusion

This project demonstrates the use of BERT for a comprehensive reading comprehension task. By fine-tuning a pre-trained BERT model on a dataset with passages, questions, and multiple answer choices, the system aims to accurately select the correct answer. The repository includes all code, dataset processing steps, and evaluation metrics required to replicate and extend the project.
