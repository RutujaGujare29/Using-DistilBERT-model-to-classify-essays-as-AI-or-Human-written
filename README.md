# Using-DistilBERT-model-to-classify-essays-as-AI-or-Human-written

**Objective**

This project is aimed at developing a sophisticated analytical model to differentiate between essays written by humans and those generated by AI. This effort is part of an initiative to maintain academic integrity by addressing the challenge posed by the use of language models like ChatGPT in academic settings.

**Dataset and Model Overview:**

1) The initial dataset comprised essays from middle and high school students, with a vast majority labeled as human-written. To address imbalance, additional data from Kaggle was incorporated.
   
2)The primary model used was BERT (Bidirectional Encoder Representations from Transformers), specifically a distilled version called DistilBERT, which is smaller and faster but retains about 97% of BERT's performance.

**Methodology:**

1) DistilBERT leverages knowledge distillation, a technique where a smaller model (student) learns from a larger model (teacher). This approach helps in reducing the model's size and complexity while maintaining efficacy.
    
2)Experiments were conducted to train the DistilBERT model, starting with a limited dataset to establish a baseline and then expanding the dataset to improve accuracy and model robustness.

**Results:**

Initial experiments with a small dataset achieved around 80% accuracy. After expanding the dataset and refining the training process, accuracy improved significantly.
The use of metrics like the F1 score and tools like confusion matrices demonstrated the model's ability to distinguish between human and AI-generated texts effectively, with high precision and recall.

**Applications and Limitations:**

1) Potential applications include content moderation on social media and cybersecurity, specifically in detecting AI-generated malicious content.
  
2) Limitations include the model's susceptibility to prompt engineering, dependency on data quality, and substantial computational resource requirements.
   
**Conclusion:**

The project underscores the importance of high-quality and diverse datasets for training AI models and highlights the utility of models like DistilBERT in educational and other settings to preserve the integrity of human-produced content.












Setting the input sequence length to 512
Tokenize and normalize the text inputs: Keras DistilBertPreprocessor layer
Parameters in the backbone (feature extraction part) are frozen
Training set: 67%; Test set: 33%
Optimizer: Adam with a learning rate of 5e-4
Epochs: Trained from 1 to 4
Batch Size: Finalized with 64
