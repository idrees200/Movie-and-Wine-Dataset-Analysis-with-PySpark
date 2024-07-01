# Movie and Wine Dataset Analysis with PySpark

## Table of Contents
1. [Introduction](#introduction)
2. [Setup and Installation](#setup-and-installation)
3. [Movie Dataset Analysis](#movie-dataset-analysis)
   - [Action Award-Winning Films](#action-award-winning-films)
   - [Award-Winning Actor Movies](#award-winning-actor-movies)
   - [Top Non-Award Winning Movies](#top-non-award-winning-movies)
   - [Least Popular Movies Before 1980](#least-popular-movies-before-1980)
   - [Movies Before 1990 Sorted by Title](#movies-before-1990-sorted-by-title)
4. [Wine Dataset Analysis](#wine-dataset-analysis)
   - [Schema and Summary Statistics](#schema-and-summary-statistics)
   - [Outlier Detection](#outlier-detection)
   - [Correlation Matrix](#correlation-matrix)
   - [K-Means Clustering](#k-means-clustering)
   - [Bisecting K-Means Clustering](#bisecting-k-means-clustering)
   - [Pairplot of Numeric Features](#pairplot-of-numeric-features)
5. [Dependencies](#dependencies)
6. [Usage](#usage)
7. [Results](#results)

## Introduction
This project demonstrates how to use PySpark for analyzing two datasets: a movie dataset and a wine dataset. It includes various queries and transformations to extract insights such as popular movies, award-winning movies, actor-related statistics, and clustering of wine data.

## Setup and Installation
1. **Install PySpark:**
    ```sh
    pip install pyspark
    ```

2. **Prepare Input Data:**
    - Place your input CSV files (`Movies.csv` and `wine.csv`) in the same directory as your scripts.

## Movie Dataset Analysis

### Action Award-Winning Films
- Filters movies that are of the "Action" genre and have won awards.

### Award-Winning Actor Movies
- Extracts movies with award-winning actors and lists the movies along with their directors.

### Top Non-Award Winning Movies
- Lists the top 10 non-award-winning movies based on popularity.

### Least Popular Movies Before 1980
- Lists the 10 least popular movies released before 1980.

### Movies Before 1990 Sorted by Title
- Lists movies released before 1990, sorted by title.

## Wine Dataset Analysis

### Schema and Summary Statistics
- Displays the schema and summary statistics of the wine dataset.

### Outlier Detection
- Identifies outliers in the dataset based on z-scores for numeric columns.

### Correlation Matrix
- Calculates and displays the correlation matrix between features.

### K-Means Clustering
- Performs K-Means clustering on the wine dataset and visualizes the clusters.

### Bisecting K-Means Clustering
- Performs Bisecting K-Means clustering on the wine dataset and visualizes the clusters.

### Pairplot of Numeric Features
- Generates pairplots for numeric features in the wine dataset to visualize relationships between features.

## Dependencies
- `pyspark`
- `matplotlib`
- `seaborn`

## Usage
1. **Start a PySpark Session and Load the Data:**
    ```python
    from pyspark.sql import SparkSession

    spark = SparkSession.builder \
        .appName("MovieAnalysis") \
        .getOrCreate()

    movies_df = spark.read.csv("Movies.csv", header=True, inferSchema=True)
    wine_df = spark.read.csv("wine.csv", header=True, inferSchema=True)
    ```

2. **Run the Analysis:**
    - Filter, transform, and query the data as described in the analysis sections.

3. **Show Results:**
    - Display the results of each query using the `show()` method.
    - Visualize clustering results using `matplotlib` and `seaborn`.

## Results
The output of each query will display the respective insights, such as lists of movies, actor statistics, and wine clustering results based on the analysis performed.
