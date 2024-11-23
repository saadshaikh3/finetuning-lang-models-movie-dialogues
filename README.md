# Conversational AI: Fine-Tuning Language Models with Movie Dialogues  

## Overview  
This project focuses on improving and fine-tuning two language models:  
- **Meta Llama-3.1-8B Model**  
- **Seq2Seq RNN Model with Attention**  

Using the **Cornell Movie-Dialogs Dataset**, the goal was to enhance the conversational capabilities of these models. The models were evaluated using key metrics, enabling a comparative analysis of their performance in conversational AI tasks.  

---

## Dataset  
The **Cornell Movie-Dialogs Dataset** was used, containing:  
- **220,579** conversational exchanges between **10,292** pairs of movie characters.  
- A total of **304,713** utterances.  

After preprocessing, the dataset was reduced to **53,131 sentence pairs**, ensuring efficient training.  

---

## Methodology  
### 1. Preprocessing  
- Rare words were removed to improve training efficiency.  
- Text was converted into tensor-based input and output batches.  
- A vocabulary index was maintained for text-to-index mapping.  

### 2. Model Training  
- **Seq2Seq RNN Model**:  
    - 12 different configurations were tested, varying attention mechanisms, hidden layer sizes, and encoder-decoder layers.  
    - Training spanned **4000 epochs**.  

- **Meta Llama-3.1-8B Model**:  
    - Fine-tuned using the same dataset over **60 steps**.  

### 3. Evaluation Metrics  
- **Loss**  
- **BLEU Score**  
- **Cosine Similarity**  

---

## Results Summary  
The **Seq2Seq RNN Model** with a hidden layer size of 500 and 2-layer encoder-decoder achieved the best results using the **dot attention mechanism**:  
- **BLEU Score**: 0.1152  
- **Cosine Similarity**: 0.5473  
- **Loss**: 2.4016  

---

## Future Directions  
- Further fine-tuning the **Meta Llama** model.  
- Experimenting with alternative attention mechanisms in RNN.  
- Exploring reinforcement learning for response quality improvement.  
- Incorporating human evaluations to assess conversational quality.  

---

## Files in Repository  
- **Notebook**: `model_training_and_evaluation.ipynb`  
- **Dataset**: Cornell Movie-Dialogs Dataset in movie-corpus folder

---

## Acknowledgements  
- **Cornell Movie-Dialogs Dataset**  
- **Meta Llama-3.1-8B** using Unsloth and Huggingface and **Seq2Seq RNN Frameworks** from https://pytorch.org/tutorials/beginner/chatbot_tutorial.html   
