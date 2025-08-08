Dialogue Summarization with T5
This project contains a complete pipeline for fine-tuning a pre-trained T5 transformer model to perform abstractive summarization on dialogue conversations. The model is trained on the SAMSum dataset to condense messenger-like chats into concise, human-readable summaries.

Features
Encoder-Decoder Architecture: Utilizes the t5-base model for high-quality sequence-to-sequence generation.

High Performance: Achieves a ROUGE-Lsum score of 46.48 on the SAMSum test set.

End-to-End Pipeline: Includes scripts for data loading, preprocessing, model training, and inference.

Optimized Training: Implements best practices like early stopping and gradient clipping for stable and efficient training.

Model Performance
The final model was trained for 5 epochs, with early stopping used to select the best-performing version based on the validation set. The final, unbiased scores were calculated on the held-out test set.

Metric

Score

ROUGE-1

46.51

ROUGE-2

22.00

ROUGE-Lsum

46.48

🛠Setup and Installation
To run this project, you'll need Python 3.8+ and the required libraries.

Usage
The main implementation is contained within the Notebook (.ipynb) file.

Training the Model
To train the model from scratch, open the notebook and run all cells in order. The script will:

Load the SAMSum dataset.

Preprocess and tokenize the data, adding the "summarize: " prefix.

Initialize the t5-base model.

Fine-tune the model using the Seq2SeqTrainer. Checkpoints will be saved to your specified output directory.

Generating a Summary (Inference)
Once the model is trained, you can use the summarize_dialogue function to generate summaries for new conversations.
