

## Dataset

The dataset consists of surveillance videos labeled as **Brawl** and **Peace**:

- **Brawl Videos**
- **Peace Videos**

## Model Pipeline

1. **Feature Extraction**:
   - Uses **ViT (Vision Transformer)** to extract visual features from video frames.
2. **BiLSTM Classification**:
   - A BiLSTM network processes these extracted features and classifies them as **Brawl or Peace**.
3. **Evaluation**:
   - Model is tested on unseen videos, and the results are saved in `predictions.csv`.

## Installation

Clone this repository and install dependencies:

```bash
pip install torch torchvision transformers pandas scikit-learn tqdm opencv-python seaborn
```

## Running the Model

1. **Open the Jupyter Notebook (**``**)**:

   - Run all cells step by step to train and evaluate the model.
   - Ensure `train_features.pkl` and `test_features.pkl` are in the same directory.

2. **Extracted Features**:

   - The model uses pre-extracted features from Vision Transformer (ViT):
     - `train_features.pkl` (Training Data Features)
     - `test_features.pkl` (Test Data Features)
   - These files must be loaded correctly in the notebook before training.

3. **Evaluate the Model & Generate Predictions:**

   - Running the notebook will produce `predictions.csv` containing video classifications.

## Output File: `predictions.csv`

The predictions file contains:

```
| video_id         | brawl |
|-----------------|-------|
| scene_001.mp4   | True  |
| scene_002.mp4   | False |
| fight_clip.mp4  | True  |
```

## Results

✅ **F1 Score:** **0.9349**  
✅ **Accuracy:** **93.25%**

## Deliverables

1. **GitHub Repository**
   - Includes a detailed README with running instructions and F1 score.
   - `predictions.csv` file containing predictions for test videos.
   - A demo video with the predicted number of people involved in a brawl (Bonus task).

2. **Presentation**
   - A **detailed presentation** (maximum 30 slides) covering the final approach and experiments.
   - 15-minute offline presentation + 5-minute Q&A session.

## Evaluation Metrics
The competition evaluates submissions based on the following criteria:

| Metric              | Weight |
|---------------------|--------|
| F1 Score           | 40%    |
| Presentation       | 40%    |
| GitHub Documentation | 20%    |

The bonus task (people count prediction) adds an **extra 10 points**.

## Timeline
- **Repository Submission Deadline:** March 25, 2025 (EOD)
- **Presentation Submission Deadline:** April 1, 2025 (EOD)

✅ **F1 Score:** **0.9479** ✅ **Accuracy:** **94.75%**

## Confusion Matrix

A confusion matrix is also generated to visualize model performance.
