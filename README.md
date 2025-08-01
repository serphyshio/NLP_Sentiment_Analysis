# SC4002 Group 6 Project Notebooks Overview

## 🔧 Setup Instructions

First, ensure you have the required **Word2Vec** model. This project uses the **GoogleNews-vectors-negative300** model.

- If you're using **Google Drive**, update the `PATH_TO_W2V_MODEL_DRIVE` constant with the model's path.
- For a **local setup**, modify the `PATH_TO_W2V_MODEL_LOCAL` constant instead.

> ⚠️ Note: Due to differences in preprocessing functions across different runtimes, the vocabulary and OOV size after preprocessing might differ across notebooks.  
> In the **Project Report**, we use the values from `SC4002_G6_Vanilla RNN.ipynb` as the standard reference.

---

## 📓 Notebook Descriptions

### `SC4002_G6_Vanilla RNN.ipynb`
- Implements **vanilla RNN** models with various aggregation strategies.

### `SC4002_G6_BiLSTM.ipynb`
- Implements **BiLSTM** models.

### `SC4002_G6_BiGRU.ipynb`
- Implements **BiGRU** models.
- Two settings are explored: **keep padding** and **mask padding**.

### `SC4002_G6_CNN_Tuning.ipynb`
- Trains and tunes a **CNN** model using **Optuna**.
- The `SimpleCNN` class allows choosing between:
  - **Max pooling**
  - **Mean pooling**
  - Optional **attention head** after aggregation.

### `SC4002_G6_CNN_Testing.ipynb`
- Tests the **CNN** model using the best hyperparameters found during tuning.
- Optimal hyperparameters for:
  - **Max pooling**
  - **Mean pooling**
  - **Attention head**  
  are provided in comments.

### `SC4002_G6_BERT.ipynb`
- Implements **transfer learning** using:
  - **BERT-base-cased**
  - **RoBERTa-base**
