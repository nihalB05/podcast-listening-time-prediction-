# podcast-listening-time-prediction-

🎧 Podcast Listening Time Prediction 🚀

A Machine Learning project to predict user listening duration (in minutes) for podcast episodes based on content, metadata, and engagement metrics. Built for competition-level performance with deep feature engineering and robust model optimization.
📌 Project Overview

In this project, we aim to predict how long users will listen to a podcast episode. The dataset contains metadata like episode length, genre, guest/host popularity, and sentiment.

We tackled the task using:

✅ Manual & custom preprocessing
✅ Feature engineering (cyclical time, interaction terms, podcast-level stats)
✅ Advanced modeling with XGBoost and ensemble stacking
✅ Cross-validation and hyperparameter tuning
✅ Competition-style predictions with optimized RMSE performance
📂 Dataset Summary
Column	Description
Episode_Length_minutes	Duration of the episode
Genre, Publication_Day	Categorical metadata
Host/Guest_Popularity	Popularity indicators
Number_of_Ads	Ad count per episode
Episode_Sentiment	Sentiment polarity
Listening_Time_minutes	🚨 Target variable
🔧 Preprocessing Highlights

We implemented:

    Manual preprocessing for categorical and numeric features

    Missing value imputation with indicators

    Encoding strategies: One-hot, label encoding, and OOF mean encoding

    Cyclical time encoding (hour_sin, hour_cos)

    Feature interactions:

        Host × Guest Popularity

        Ads per Minute, Length × Ads

        Weekend × Time of Day

🧠 Modeling Approach
✅ Models Used:

    XGBoost Regressor 🔥

    LightGBM & CatBoost for stacking

    Ridge as meta-model (stacking layer)

⚙️ Optimization:

    5-Fold Cross-Validation

    RandomizedSearchCV for tuning

    Ensemble stacking for final predictions

📉 Evaluation Metric:

    Root Mean Squared Error (RMSE)

    Best RMSE achieved (CV): ~13.07

    Benchmark leaderboard RMSE: 11.44

📈 Key Results & Learnings

    ⚙️ Engineering OOF target means for podcasts added significant lift

    🧩 Interactions + time features reduced overfitting

    🧪 Stacking consistently outperformed single models

    🎯 Final submission was robust and close to the top leaderboard entries

📁 Folder Structure

📦 podcast-listening-prediction/
│
├── 📘 README.md
├── 📒 pplt.ipynb              # Main notebook
├── 📊 submission.csv          # Final output
├── 📁 data/                   # Train & test datasets
└── 📎 requirements.txt        # Required libraries

🚀 How to Run

    Clone the repo

git clone https://github.com/yourname/podcast-listen-time
cd podcast-listen-time

Install dependencies

    pip install -r requirements.txt

    Run the notebook
    Open pplt.ipynb in Jupyter Notebook or VS Code and execute step-by-step.

📌 Future Improvements

    Add NLP-based sentiment reanalysis from titles

    Use audio metadata (if available)

    Try neural networks (MLP or TabNet)

    Add SHAP explainability

🧠 Author

Your Name — Data Science Enthusiast | ML Explorer 🚀
Feel free to connect or contribute ideas!
