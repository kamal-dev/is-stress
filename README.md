# Tweet Analysis to check if the user is stressed

## Create the environment
    Install python on your system
    Install Anaconda or mini Conda in your system
    Create a virtual environment:
        1. conda create -p venv python==3.9
        2. conda activate venv/ 

## Project Setup:
    pip install -r requirements.txt

## Directory Structure:
    |- assets                       --- This contains the pickle file
        |- hashtag_pipeline.pkl
        |- text_pipeline.pkl
    |- data
        |- twitter_stress.xlsx      --- Contains the dataset used in this project [/kaggle/input/stress-detection-from-social-media-articles/Twitter_Full.csv]
    |- .gitignore
    |- model.ipynb                  --- Contains the jupyternotebook where basic EDA, feature engineering and model training was done
    |- README.md
    |- requirements.txt             --- Libraries Required to run this project

## Algorithms used

Our problem statement here was the classification problem with dataset to identify from a tweet, whether a person is stressed or not. To achieve this, initially I used CountVector to vectorize the text data as I had planned to use Logistic Regression for this. 

Post the vectorization I used AdaBoostClassifier with LogisticRegression as the classifier. I decided to go with the AdaBoostClassifier along with LogisticRegression as the data we were trying to train and test was a text data. And it might have not performed well with the LogisticRegression. Plus using an Ensemble learning method like AdaBoostClassifier has multiple benefits over using the Classification model directly like - Better performance by combining multiple weak learners, handling complex dataset, robustness to overfitting as well as better generalization.


![Equation](https://latex.codecogs.com/svg.latex?\log%20\left(%20\frac{p(y=1)}{1-p(y=1)}%20\right)%20=%20\beta_0%20+%20\beta_1%20x_1%20+%20\beta_2%20x_2%20+%20\ldots%20+%20\beta_n%20x_n)