# Star Wars Dialogue Generation

The project aims to implement a Text Generation model to generate dialogue texts of different Star Wars characters given a seed sentence. The model intends to generate text for characters - Obi-wan Kenobi (Human interpretable sentences), Yoda(Reverse grammar sentences) and C3PO(Droid like sentences). The folder structure for the project is as below:

1. Data - Orginal star wars scripts
2. Filtered Data - Filtered scripts for the above three characters
3. Python Notebooks - 
                     
      ~ Read the original data files (kaggle .txt files and IMSDB HTML links)
      
      ~ Basic word sequence input neural network
                     
      ~ Sliding Window LSTM
                     
      ~ Sliding Window Bidirectional LSTM
                     
      ~ Sliding Window Bidirectional LSTM with GLOVE
                     
     ~ Sliding Window Bidirectional LSTM with GLOVE with returning sequence
     
4. Final models - Contains the executable python notebook to run for each character for text generation and mood detection
5. Results - Output text files (contains generated text and bleu score)

## Input Data:

Our data is derived from the Kaggle star wars script data and IMSDB scripts. The links to both are available here:

~ https://imsdb.com/search.php

~ https://www.kaggle.com/xvivancos/star-wars-movie-scripts

The scripts are filtered for characters and reformatted into a two-column Dataframe (character, dialogue). These filtered dataframes are stored in the "Filtered Data" folder.

## Running the Models:

- The final model used is "Sliding Window Bidirectional LSTM with GLOVE with returning sequence" and can be accessed from the Models folder. It is preferred to use Google Colab for running the models using GPU (These computationally expensive models and will be slow on the local machine). 
- The models are written in python notebooks (.ipynb) and simply require a run of all the cells.
- Each notebook also contains comments to help navigate and understand what is happening in each cell.

## Results:

- The results are stored in the "Results" folder. The output is generated from selecting random input sequences from the training data itself. The model predicts the next best word to be added to the seed sentence. 
- the output is stored in the following format:
  
\<Generated Final Sentences\>
  
 ....
 
BLEU score for \<character name\> \-\> \<value\>

  
  
