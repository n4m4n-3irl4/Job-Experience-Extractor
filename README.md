# Job Description Experience Extractor

## Project Overview
A Python tool that extracts "total experience required" from job descriptions using state-of-the-art NLP models. Compares results from:
- **spaCy Transformer NER**
- **BERT Question Answering**
- **Flair TARS Zero-Shot Classification** 
- **RoBERTa Token Classification**

---

## Best Model Recommendation

### **Best Performing Model**: BERT Question Answering

### Why BERT QA Works Best:
1. **Contextual Precision**  
   Understands phrasal variations like _"5+ yrs exp"_ vs _"minimum three years experience"_
2. **Question-Driven Focus**  
   Explicit query _"What is the total experience required?"_ filters irrelevant numbers
3. **Confidence Thresholding**  
   Built-in scoring (accepts answers >0.1 confidence) reduces false positives

### Comparison Challenges:
| Challenge                | Impact                          | Mitigation                     |
|--------------------------|---------------------------------|--------------------------------|
| Format variability        | "3-5 yrs" vs "2+ years"        | Output normalization          |
| Experience vs Tenure      | Project dates vs job experience | Contextual pattern matching    |
| Model resource needs      | Large RAM/CPU requirements      | Batch processing               |

---

## 🛠 Setup & Execution

### Step 1: Environment Setup
```bash
# Create virtual environment
python -m venv env

# Activate environment
source env/bin/activate      # Linux/Mac
.\env\Scripts\activate       # Windows
```

### After this, you can place the job descriptions excel file in the project directory and run the ipynb notebook, which will output the required excel file.