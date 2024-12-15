# Predicting Song Popularity with Machine Learning

## Final Project Code
The complete project code is available on [GitHub](https://github.com/krackalackel02/Datafy/blob/main/M148_Project.ipynb).
## Data Set
**Data Source:** Spotify  
We utilized the `spotify-tracks-dataset` provided by user maharshipandya on the Hugging Face platform. The dataset contains 114,000 rows, with each row representing a song and its features. The data was collected and cleaned using Spotify's API and Python.  
**Link to Dataset:** [spotify-tracks-dataset](https://huggingface.co/datasets/maharshipandya/spotify-tracks-dataset)

### Dataset Features
- **track_id**: Spotify ID for the track
- **artists**: Names of performing artists (separated by `;` if multiple)
- **album_name**: Album name containing the track
- **track_name**: Name of the track
- **popularity**: A value (0-100) indicating track popularity
- **duration_ms**: Track length in milliseconds
- **explicit**: Explicit content flag (`true`/`false`)
- **danceability**: Suitability of a track for dancing (0.0 to 1.0)
- **energy**: Measure of intensity and activity (0.0 to 1.0)
- **key**: Musical key of the track (0 = C, 1 = C♯/D♭, ..., -1 = No key detected)
- **loudness**: Track loudness in decibels (dB)
- **mode**: Modality of the track (`1` = Major, `0` = Minor)
- **speechiness**: Presence of spoken words (0.0 to 1.0)
- **acousticness**: Confidence that the track is acoustic (0.0 to 1.0)
- **instrumentalness**: Likelihood of no vocals (0.0 to 1.0)
- **liveness**: Presence of an audience in the recording (0.0 to 1.0)
- **valence**: Musical positivity of a track (0.0 to 1.0)
- **tempo**: Estimated tempo in beats per minute (BPM)
- **time_signature**: Estimated time signature (3 to 7 for 3/4 to 7/4)
- **track_genre**: Genre of the track

---

## Problem of Interest
Our objective was to predict a song's popularity based on its features. We explored relationships between variables through exploratory data analysis (EDA) and trained various machine learning models to address this task.

---

## Methodology and Results

### Exploratory Data Analysis (EDA)
EDA revealed minimal direct correlations between individual features and popularity (maximum correlation ≈ 0.05). This necessitated advanced modeling techniques to capture complex interactions.

### Models Evaluated
#### 1. **K-Nearest Neighbors (KNN)**
- **Test Accuracy:** 56.8%
- **5-Fold Cross-Validation AUC:** 0.5803  
- **Limitations:** Poor performance due to high-dimensional data and weak feature-target correlations.

#### 2. **Random Forest**
- **Validation Accuracy:** 66.5%
- **Test Accuracy:** 66.0%
- **Test AUC:** 0.7085  
- **Strengths:** Handled feature complexity well and reduced overfitting.  
- **Weaknesses:** Limited by weak correlations and inability to capture intricate patterns.

#### 3. **Neural Network**
- **Test Accuracy:** 78%
- **Architecture:**
  - ReLU activation in hidden layers
  - Sigmoid activation in output layer
- **Training/Validation Loss:** Steady decrease, no overfitting  
- **Strengths:** Captured non-linear relationships effectively, outperforming other models.

---

## Conclusions
The **neural network** outperformed other models due to its ability to model non-linear interactions, achieving the highest accuracy (78%). While the random forest model provided a robust alternative with moderate accuracy (66%), KNN struggled due to the dataset's high dimensionality.

**Key Takeaway:** Predicting song popularity is a complex task that requires sophisticated models like neural networks to capture subtle and non-linear relationships in the data.

---

## How to Use the Code

###Steps to Run
1. Clone the repository:

```bash
git clone https://github.com/cadencechang/Datafy_Final.git
```

2. Run the code:
Prese Run all in notebook editor






