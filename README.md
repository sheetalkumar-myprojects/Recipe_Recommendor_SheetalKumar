# Recipe_Recommendor_SheetalKumar
Recipe Recommendation System Using TF-IDF, KNN, and PCA
Overview

This project builds a Recipe Recommendation System that suggests recipes based on the ingredients a user already has.

Using Natural Language Processing (NLP) techniques and Machine Learning, the system:

Converts ingredient lists into numerical vectors using TF-IDF

Finds similar recipes using K-Nearest Neighbors (KNN)

Visualizes ingredient similarity using Principal Component Analysis (PCA)

 Problem Statement

Users often struggle to decide what to cook with the ingredients available at home. Manually searching for recipes is time-consuming.

This system recommends the most similar recipes based on user-provided ingredients.

 Project Objectives

Recommend recipes based on available ingredients

Find the top k most similar recipes

Visualize recipe similarity in 2D space

Build a scalable foundation for future enhancements

 Dataset Description

The dataset contains structured recipe information with the following fields:

Title – Recipe name

Ingredients – List of ingredients

Instructions – Cooking instructions

YouTube Link – Video reference

Example Entry:
Title: Classic Grilled Cheese  
Ingredients: bread, cheese, butter  
Instructions: Butter bread, add cheese, grill.
 Data Preprocessing

Steps performed:

Removed rows with missing values

Converted ingredient text to lowercase

Removed special characters

Standardized ingredient formatting (comma-separated)

This ensures clean and consistent input for vectorization.

 TF-IDF Vectorization
What is TF-IDF?

TF-IDF (Term Frequency – Inverse Document Frequency) converts text into numerical vectors.

In this project:

Ingredients are treated as text data

A custom tokenizer splits ingredients by commas

Each recipe is represented as a high-dimensional vector

Output:
A sparse matrix representing ingredient importance.

 K-Nearest Neighbors (KNN)

Model: NearestNeighbors from scikit-learn

Similarity Metric: Cosine Similarity

Algorithm: Brute-force search (suitable for small datasets)

The system:

Converts user input into TF-IDF vector

Computes similarity

Returns top 3 closest recipes

Example Input:
bread, cheese
Example Output:

Classic Grilled Cheese

French Toast

Egg Salad Sandwich

 Principal Component Analysis (PCA)

Because TF-IDF produces high-dimensional vectors, PCA is applied to:

Reduce dimensions to 2D

Visualize recipe similarity

Show clusters of similar recipes

 Visualization

The system generates a 2D plot:

Blue dots → Recipes

Red X → User input

➖ Dashed lines → Connections to nearest recipes

Labels → Recipe titles

Tool used: matplotlib

Project Workflow

Upload Dataset

Data Cleaning

TF-IDF Vectorization

Train KNN Model

Accept User Input

Find Recommendations

Apply PCA

Plot Results

⚠ Challenges Faced

Handling inconsistent ingredient formatting

Avoiding overlapping labels in visualization

Matching user input consistently with dataset entries

Future Improvements

Interactive UI (web interface or app)

Use advanced embeddings (e.g., BERT)

Add filters (dietary restrictions, cooking time)

Improve dynamic visualization

Integrate with recipe APIs

Conclusion

This project successfully:

Recommends recipes based on ingredient similarity

Applies NLP and ML techniques effectively

Visualizes similarity relationships

Provides a scalable base for future development

🛠 Technologies Used

Python

Pandas

Scikit-learn

Matplotlib

TF-IDF

KNN

PCA
