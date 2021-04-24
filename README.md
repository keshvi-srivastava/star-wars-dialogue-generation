# Star Wars Dialogue Generation

The project aims to implement a Text Generation model to generate dialogue texts of different Star Wars characters given a seed sentence. The model intends to generate text for characters - Obi-wan Kenobi (Human interpretable sentences), Yoda(Reverse grammar sentences) and C3PO(Droid like sentences). The folder structure for the project is as below:

1. Original Kaggle Data - Original .txt files from kaggle
2. Data - All filtered star wars scripts
4. Filtered Data - Filtered scripts for the three characters
5. Python Notebooks - 
      
      ~ Basic word sequence input neural network
                     
      ~ Sliding Window LSTM
                     
      ~ Sliding Window Bidirectional LSTM
                     
      ~ Sliding Window Bidirectional LSTM with GLOVE
                     
      ~ Sliding Window Bidirectional LSTM with GLOVE with return_sequence

      ~ Mood detection ???
      
6. Final notebooks - Contains the executable python notebook to run for text generation and mood detection
              
      ~ Read_data.ipynb -> Read the original data files (kaggle .txt files and IMSDB HTML links)
      
      ~ Text_Generation_Model.ipynb -> Generate dialogues
      
      ~ Mood detection ??
      
7. Results - Output text files (contains generated dialogues with bleu score and mood detected for dialogues)

## Input Data:

Our data is derived from the Kaggle star wars script data and IMSDB scripts. The links to both are available here:

~ https://imsdb.com/search.php

~ https://www.kaggle.com/xvivancos/star-wars-movie-scripts

The scripts are filtered for characters and reformatted into a two-column Dataframe (character, dialogue). These filtered dataframes are stored in the "Filtered Data" folder.

Obiwan (Ben)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Human	  :	583 dialogues

Yoda&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Alien  	:	168 dialogues

C3-PO (Threepio)&nbsp;&nbsp;&nbsp;&nbsp;- Droid	  : 358 dialogues

## Running the Final Model Notebooks:

- To generate the data, run the Read_data.ipynb. It requires the data from 'Original Kaggle Data' folder and access to HTML links. Detailed comments added to the notebook.
- The final model used is "Sliding Window Bidirectional LSTM with GLOVE with return_sequence" and can be accessed from the 'Final notebooks' folder. It is preferred to use Google Colab for running the models using GPU (These computationally expensive models and will be slow on the local machine). 
- The models are written in python notebooks (.ipynb) and simply require a run of all the cells.
- To test for mood detection run _____________________________________. \<To be filled\>
- Each notebook also contains comments to help navigate and understand what is happening in each cell.

## Results:

- The results are stored in the "Results" folder. The output is generated from selecting random input sequences from the training data itself. The model predicts the next best word to be added to the seed sentence. 
- The output is stored in the following format:
  
\<Generated Final Sentences\>
  
 ....
 
BLEU score for \<character name\> \-\> \<value\>

- The output for mood detection ________________ \<To be filled\>
  
  
