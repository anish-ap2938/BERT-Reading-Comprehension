# BERT-Reading-Comprehension
BERT-Reading Comprehension
The model's task is to read a passage and select the correct answer based on its content.

![image](https://github.com/user-attachments/assets/6cc52c94-2580-4703-9b89-218236637c53)

Fine-tuning a BERT model means taking a pre-trained BERT model and training it further
on a specific task, for this task, we need do it on reading comprehension.

Dataset
● Download data https://drive.google.com/file/d/1LABaYT-2gWthtNnW7PKlG9pM8Mh3NvuA/view
○ Each dataset includes a question ID, context, the question text, three answer
choices, and a label indicating the correct choice number
○ train_data.csv (8488, 7)
○ test_data.csv (2122, 7)

■ The label for the test dataset is “Null”
We used : i. bert-base-uncased
ii. bert-large-uncased
Output format:
● .csv file
● The submission file includes two columns:
○ id: 0,1,2, etc
○ label: 0,0,1, etc

Evaluation metric: Categorization Accuracy
