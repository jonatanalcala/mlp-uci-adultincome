# MLP Application on UCI Adult Income Dataset

This project implements and evaluates an MLP algorithm using the **UCI Adult Income dataset** to predict whether an individual earns more than $50K/year. This is a python based project primarily using PyTorch for building the model.

---

## 📂 Project Structure
```text
mlp-uci-adultincome/
├─ README.md
├─ requirements.txt                                    # Python dependencies             
├─ LICENSE
├─ docs/                                               # Research & Key concepts, presentation (.pdf)
├─ data/
│  ├─ raw/                                             # project_adult.csv, project_validation_inputs.csv (read-only)
│  └─ processed/                                       # cleaned & encoded datasets, train/val splits
├─ notebooks/
│  ├─ 01_preprocess.ipynb                              # Part 1: missing, encode, standardize
│  └─ 02_mlp.ipynb                                     # Part 2: Multilayer Perceptron
├─ outputs/                                            # Model prediction for MLP model                                
│  ├─ Group_18_MLP_PredictedOutputs.csv
│  └─ graphs/                                          # Loss/Accuracy Curves, Confusion Matrix, etc. 
```

---

## Features

- **Preprocessing**
  - Handle missing values with imputations
  - Encode categorical features
  - Standardize numerical features

- **MLP Implementation w/ PyTorch**
  - Defining, training, and evaluting MLP using `nn.Module`
  - Activation function(s)
  - Model architecture (e.g., number of layers)
 
- **Visualization**
  - TO DO

- **Refelction**
  - Evaluating MLP Architecture
  - Monitoring & Mitigating Overfitting
  - Ethical Concerns
  - Actication Functions
 
---

## Deliverables
- Python source code + Jupyter notebooks  
- Prediction CSVs (Validation Output File)
  - Provided outputs are transformed using the following function: `1 if x == '>50K' else -1`
- Figures for learning curves and other data visualizations
- 15-minute recorded presentation with slides  
- Written reflection on algorithm behavior  

## Data
- `project_adult.csv`  
- `project_validation_inputs.csv`  
- Source: [UCI Adult Income Dataset](https://archive.ics.uci.edu/dataset/2/adult)  

---

## Results

**MLP Implementation**
- TO DO

---

## ⚙️ Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/mlp-uci-adultincome.git
   cd ml-classification
2. **Create a virtual environment & install dependencies**
    ```bash
    python -m venv venv
    source venv/bin/activate     # Mac/Linux
    venv\Scripts\activate        # Windows

    pip install -r requirements.txt
    ```
3. **Run Notebooks**
    ```bash
    jupyter notebook

    ```
