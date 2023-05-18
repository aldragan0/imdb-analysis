# IMDB Movie analysis
This repository provides an analysis of the IMDB dataset, data available [here](https://developer.imdb.com/non-commercial-datasets/). A detailed description about the content of the datasets can be found on the official site. A summarized version is available in `metadata.txt`.

Note: The datasets are regularly updated daily as new movies are released. The datasets in this repo were retrieved on 3rd March 2023. Your results might vary.

The data used in this project is provided in `data.zip` as a single *.csv* file for reproducibility purposes.
The data provided in `data.zip` is under the same license as the original data provided by IMDB.

Information courtesy of
IMDb
(https://www.imdb.com).
Used with permission.

## Running the code
* Install conda/miniconda
* Create new env and install the requirements - `conda create --name imdb-analysis --file requirements.txt`
* `conda activate imdb-analysis`
* Start your preferred jupyter notebook editor and load `main.ipynb`

## Analysis goal
The goal of this project is to find a proper model the movie's average rating.

## Project outline
The project is split into 5 main parts.

### 1. Loading the clean data
This is mostly for convenience/reproducibility, instead of loading and cleaning all the data every time you can just load the clean data and continue with the analysis.

### 2. Loading the raw data
This part is self-explanatory, here we load and preview the raw data from IMDB.
Note: raw IMDB data comes as `.gz` files so you have to deflate it first.

### 3. Cleaning the data
Here we process/transform and clean the data. The purpose of data transformation was to optimize the dataset size (since the datasets are quite big). Next we clean the data, handling missing values and then join all the datasets into one big DataFrame.

Note that some of the data cleaning (fixing incorrect values) was done manually in the datasets themselves. There are comments in `main.ipynb` explaining the manual steps taken.

### 4. Overview of all the movie data
In the previous section we've joined all the separate datasets into one. The purpose of this section is to provide some insights into that data.

### 5. Exploratory data analysis of the movies
This section analyzes the data about movie titles (movie/tvMovie).
We've started this section with univariate analysis, describing individual variables, moving on to bivariate analysis, where we assessed the variable correlations.
We concluded by investigating if the movie's average rating can be modeled using a multivariate linear regression model containing the features we've found to be relevant in the previous stages.
