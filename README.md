# Smart-Grid-Electricity-Theft-Detection
Smart Grid Electricity Theft Detection Powered by Machine Learning and Advanced Consumption Pattern Analysis


```mermaid
graph TD;
    A[Start] --> B[Load Dataset]
    B --> C[Check Dataset Info & Summary]
    C --> C1[Display First Few Rows]
    C --> C2[Check Data Types]
    C --> C3[Check Summary Statistics]
    C --> C4[Check Missing Values]

    C4 -->|If Missing Data Exists| D1[Handle Missing Values]
    C4 -->|No Missing Data| E

    D1 -->|Fill or Drop| D2[Impute or Remove Data]
    D2 --> E[Data Preprocessing]

    E -->|Feature Scaling| F[Apply MinMax Scaler]
    E -->|Label Encoding| G[Encode Categorical Variables]
    E -->|Check Correlations| H[Plot Heatmap]

    F --> I[Train-Test Split]
    G --> I
    H --> I

    I -->|Training Set| J[Model Training]
    I -->|Testing Set| O[Model Evaluation]

    J -->|KNN| J1[K-Nearest Neighbors]
    J -->|Decision Tree| K1[Decision Tree Classifier]
    J -->|Random Forest| L1[Random Forest Classifier]
    J -->|Bagging| M1[Bagging Classifier]
    J -->|MLP| N1[Neural Network Classifier]

    J1 --> O
    K1 --> O
    L1 --> O
    M1 --> O
    N1 --> O

    O -->|Accuracy| P1[Calculate Accuracy Score]
    O -->|F1 Score| P2[Calculate F1 Score]
    O -->|Kappa Score| P3[Calculate Cohen Kappa Score]
    O -->|ROC-AUC| P4[Calculate ROC-AUC Score]

    P1 --> Q[Compare Model Performance]
    P2 --> Q
    P3 --> Q
    P4 --> Q
    Q --> R[End]

```