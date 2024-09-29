# Link to Access the Colab Notebook : https://colab.research.google.com/drive/1JpKBhe9iJFHlsniCY53WdgbPURWajvz1?usp=sharing
# **Cross-Lingual Word Embedding Alignment**

**Author:** Pranjal Chaubey (prnjlchaubey@gmail.com)  
*Created using Lightning AI Studio and shared via Colab*

---

## **Overview**
This notebook demonstrates the process of aligning cross-lingual word embeddings using a supervised approach. The task focuses on aligning English and Hindi word embeddings using the **Procrustes method** and evaluates the quality of alignment.

The notebook is organized into three main steps:

---

### **Step 1: Data Preparation**
1. **Loading Pretrained Embeddings**:  
   - Using FastText embeddings, we limit the vocabulary to the top 100,000 words for both languages.
   
2. **Creating Word-Vector Dictionary**:  
   - Construct dictionaries that map the top words to their corresponding word vectors.

3. **Loading Bilingual Dataset**:  
   - Fetching and filtering the **English-Hindi bilingual dataset** from the MUSE repository.

---

### **Step 2: Embedding Alignment**
1. **Procrustes Alignment**:  
   - Performing the Procrustes alignment to align embeddings of the two languages.  
   - Ensuring that the transformation matrix \(W\) is orthogonal.

2. **Visualization**:  
   - Visualizing the word vectors both before and after alignment using **PCA** to observe how well the alignment has adjusted the vectors.

---

### **Step 3: Evaluation**
1. **Training Set Evaluation**:  
   - Calculating **Precision@1** and **Precision@5** using the aligned word embeddings on the training dataset.

2. **Test Set Evaluation**:  
   - Testing the alignment on the MUSE test dataset by calculating **Precision@1** and **Precision@5**.

3. **Qualitative Examples**:  
   - Verifying the alignment results with concrete word pair examples.

---

### **Summary of Results**
- **Precision@1**: 0.309  
- **Precision@5**: 0.617

