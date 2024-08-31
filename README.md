
# Multi-Label Text Classification Project

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Project Structure](#project-structure)
4. [Preprocessing](#preprocessing)
5. [Modeling](#modeling)
6. [Evaluation](#evaluation)
7. [Results](#results)
8. [Conclusion](#conclusion)

## Project Overview
Classification is a crucial task in real-world applications, particularly in the context of text analysis. With the massive amount of text generated every second in the form of blogs, posts, and articles, predicting information about the author based on their writing becomes a significant challenge.

In this project, we have created a classifier to predict multiple features of an author from a given text, treating it as a multi-label classification problem. The features to be predicted include the author's gender, age, industry, and astrological sign.

## Dataset
The dataset used in this project is the **Blog Authorship Corpus**, which consists of over 600,000 posts from more than 19,000 bloggers. The corpus was gathered from blogger.com in August 2004 and includes:
- **681,288 posts**
- **140 million words** (~35 posts and 7250 words per person)
- **19,320 bloggers** categorized into gender, age, industry, and astrological sign.

Each blog file is labeled with the blogger's gender, age, industry, and astrological sign, although some entries have missing labels for industry and sign.

**Link to Dataset**: [Blog Authorship Corpus on Kaggle](https://www.kaggle.com/rtatman/blog-authorship-corpus)

## Project Structure
The project is structured as follows:
- **`data/`**: Contains the dataset (if included) or a link to download it.
- **`notebooks/`**: Jupyter notebooks for data exploration, preprocessing, and modeling.
- **`scripts/`**: Python scripts for data preprocessing and model training.
- **`models/`**: Saved models and results.
- **`README.md`**: Project documentation.
- **`requirements.txt`**: List of Python packages required to run the project.

## Preprocessing
The preprocessing steps involve:
1. **Loading the Dataset**: Reading the CSV file with explicit encoding and quoting settings.
2. **Cleaning the Text**: Removing unwanted characters, converting text to lowercase, removing extra spaces, and removing stopwords.
3. **Merging Labels**: Combining the labels (`gender`, `age`, `topic`, and `sign`) into a single column for multi-label classification.

## Modeling
We used a multi-label classification approach:
1. **Splitting Data**: The data is split into training and testing sets.
2. **Vectorization**: Features are vectorized using the Bag of Words approach with `CountVectorizer` and `ngram_range=(1,2)`.
3. **Label Transformation**: Labels are transformed into a binary format using `MultiLabelBinarizer`.
4. **Classification**: We implemented the One-vs-Rest approach using `LogisticRegression` to handle multi-label classification.

## Evaluation
We evaluated the model using the following metrics:
- **Accuracy Score**
- **F1 Score**
- **Average Precision Score**
- **Average Recall Score**

## Results
The model was tested on a subset of 1000 entries from the dataset. The results include:
- Accuracy: [Add result]
- F1 Score: [Add result]
- Average Precision: [Add result]
- Average Recall: [Add result]

Additionally, the true and predicted labels for five sample entries were compared to assess the model's performance.

## Conclusion
This project demonstrates the feasibility of predicting multiple author attributes from blog text using multi-label classification. The results show that logistic regression, coupled with the One-vs-Rest strategy, can be an effective approach for this type of problem. Further improvements can be achieved by exploring more advanced models and fine-tuning hyperparameters.

---

You can replace `[Add result]` with your actual results from the project. This template should provide a clear and structured documentation of your project for anyone who views your GitHub repository.
