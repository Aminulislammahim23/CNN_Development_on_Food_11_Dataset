# Food-11 CNN Image Classification
 
A PyTorch-based deep learning project for multi-class food image classification on the Food-11 dataset.
 
This repository contains a complete notebook pipeline for:
- Data loading and preprocessing
- Data augmentation
- Training and validation
- Comparing two custom CNN models
- Test evaluation with classification metrics
- Visualization of training curves, confusion matrix, and per-class F1
- Saving trained model weights
 
## Project Summary
 
The notebook trains and compares two CNN architectures:
- Model A: Baseline CNN (no BatchNorm, no Dropout)
- Model B: Regularized CNN (BatchNorm + Dropout)
 
Experiment settings used in the notebook:
- Input size: 128x128
- Epochs: 20
- Batch size: 32
- Optimizer: Adam
- Scheduler: ReduceLROnPlateau
 
## Dataset
 
The project uses Food-11 with 11 classes:
- Bread
- Dairy_product
- Dessert
- Egg
- Fried_food
- Meat
- Noodles_Pasta
- Rice
- Seafood
- Soup
- Vegetables_Fruit
 
Current split sizes in this repository:
- Train: 3,347 images
- Validation: 3,347 images
- Test: 3,347 images
 
## Final Results (from notebook output)
 
| Metric | Model A | Model B |
|---|---:|---:|
| Accuracy | 0.4649 | 0.4398 |
| Precision (macro) | 0.4659 | 0.4959 |
| Recall (macro) | 0.4211 | 0.3855 |
| F1 (macro) | 0.4156 | 0.3717 |
 
Best model by macro F1 in this run: **Model A**.
 
## Repository Structure
 
```text
Food-11-CNN/
  data/
    train/
    val/
    test/
  notebooks/
    CNN_22_46183_1.ipynb
    class_distribution.png
    sample_images.png
    training_curves.png
    confusion_matrix.png
    per_class_f1.png
    predictions_model_a.png
    predictions_model_b.png
  outputs/
    model_a_best.pth
    model_b_best.pth
    assignment_text.txt
    notebook_cells_dump.txt
```
 
## How to Run
 
1. Create and activate a Python virtual environment.
2. Install dependencies.
3. Open the notebook and run all cells.
 
Example (Windows PowerShell):
 
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install torch torchvision numpy matplotlib seaborn scikit-learn jupyter
cd notebooks
jupyter notebook CNN_22_46183_1.ipynb
```
 
Note: Run Jupyter from the `notebooks/` directory so the notebook path logic correctly resolves `../data`.
 
## Outputs
 
- Trained weights are saved to `outputs/`:
  - `model_a_best.pth`
  - `model_b_best.pth`
- Evaluation visuals are saved in `notebooks/`:
  - `training_curves.png`
  - `confusion_matrix.png`
  - `per_class_f1.png`
  - Prediction samples for both models
 
## Notebook
 
Main notebook:
- `notebooks/CNN_22_46183_1.ipynb`
 
This notebook includes model definitions, training logs, evaluation reports, and discussion of best/worst performing classes.
