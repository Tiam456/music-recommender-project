# ST446 course project

## Project task

In this project, we developed a music recommendation system by using the Neural Collaborating Filtering (NCF) model and Dimension Independent Matrix Square with MapReduce (DIMSUM) algorithm within a distributed computing framework. The NCF model replaced the state-of-the-art method in matrix factorization models, which applies the inner product to the latent features of users and items, with a neural network that extracts underlying concealed patterns from the data. On the other hand, the DIMSUM algorithm defines an efficient method for calculating the similarity between items using a MapReduce framework and a large and sparse user-item matrix. We developed the NCF model to build a recommendation system and evaluated the ability of the model and applied the DIMSUM algorithm in distributed framework to assess the impact of distribution of computation in building efficient algorithm to compute similarity between items.   

## Data source  
https://www.aicrowd.com/challenges/spotify-million-playlist-dataset-challenge   

## How to read this repository  

### Data Loading and preprocessing  
Please refer to the notebook LoadData_1 and EDA_2.   

### NCF model   
NCF_model: this notebook contains our the codes of our model.   
NCF_trainingScript: this is a ntoebook of our experimentation on testing the model with different hyperparamters. It contains the same code as NCF_model, hence we did not make annotation.   
NCF_evaluations: This file constains the the script of how we evaluate our model.   
NCF_PlotLosses and NCF_PlotPredictions: This two files contain the code of hwo we generate the plots in our report.   
test_DF and trainWnegative61: our test and train set after preprocessing.   
NCF_evaluation_results: the data we included in the appendix section of our report.   

### NCF Model training history  
This folder contains our model training loss and predictions. We use npy file format to store our model predictions on test set corresponding to different hyperpameter settings and pkl file to store the model history.   

### DIMSUM model  
To look at the code of the model, please refer to Editted_DIMSUM_Model.   
DIMSUM model: this notebook consists of the details of how we build our model.   
Editted_DIMSUM_Model: this notebook is a duplicate of DIMSUM model but we removed the error messages by Spark resource allocator to make the notebook more presentable.   
DIMSUM_model_plot: this notebook consists of codes of how we plot our experiment results.   
DIMSUM_comparison and DIMSUM_impact_results: this two files contain the results from our experiment. The results in the first file is about the comparision of efficiency of the computation across different configuration while the second file has information about the efficiency of the algorithm when we experiment with restricting the growth of number of columns to be lower than the growth of number of rows.     

### DIMSUM output    
This folder contains the ouput of the DIMSUM algorithm. The indexing after underscore syntax in the file name represents the correpsonded hyperparameter values. We only include the top 1000 rows of the outputs for every iteration as the data szie is too big to upload to github.     





