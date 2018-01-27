# CSX_450_1_Project_2 - Geographical Origin of Music    



## The Domain of the Problem

  The dataset contains collection of 1059 tracks covering 33 countries. The music used is traditional, ethnic or `world' only, as classified by the publishers of the product on which it appears. Any Western music is not included because its influence is global - what we seek are the aspects of music that most influence location. Thus, being able to specify a location with strong influence on the music is central. 

  The geographical location of origin was manually collected the information from the CD sleeve notes, and when this information was inadequate other information sources were searched. The location data is limited in precision to the country of origin. 

  The country of origin was determined by the artist's or artists' main country/area of residence. Any track that had ambiguous origin is not included. We have taken the position of each country's capital city (or the province of the area) by latitude and longitude as the absolute point of origin. 

  The program **_MARSYAS[1]_** was used to extract audio features from the wave files. Default MARSYAS settings is used in single vector format (68 features) to estimate the performance with basic timbal information covering the entire length of each track. No feature weighting or pre-filtering was applied. All features were transformed to have a mean of 0, and a standard deviation of 1. We also investigated the utility of adding chromatic attributes. These describe the notes of the scale being used. This is especially important as a distinguishing feature in geographical ethnomusicology. The chromatic features provided by MARSYAS are 12 per octave - Western tuning, but it may be possible to tell something from how similar to or different from Western tuning the music is. 

  **_[1] G. Tzanetakis and P. Cook, â€œMARSYAS: a framework for audio analysis,â€ Organised Sound, vol. 4, pp. 169â€“175, 2000_**

   

**_Creators of the Dataset:_** 
  _Fang Zhou (fang.zhou@nottingham.edu.cn)_ 
  _The University of Nottinghan, Ningbo, China_ 

**_Donors of the Dataset:_** 
  _Fang Zhou (fang.zhou@nottingham.edu.cn)_ 
  _Claire Q (eskoala@gmail.com)_ 
  _Ross D. King (ross.king@manchester.ac.uk)_


  In the following publication, this dataset was used to investigate, training a machine learning program to predict the geographical origin of pieces of music. The authors used K-Nearest Neighbors(KNN) and Random forest regression and their experimental results indicate that Random forest regression produces significantly better results than KNN, and the use of bagging improves the performance of KNN.
  
  **
   Fang Zhou, Claire Q and Ross. D. King 
   Predicting the Geographical Origin of Music, ICDM, 2014 **



## Problem Statement

    Given a piece of music that is traditional, ethnic or `world' only, we can build Machine learning to identity and choose the geographic area that scores the highest in terms of the features associated with the piece of music and output that location as the the Origin of the Music track input. 
    Machine learning has to be developed for various combinations of features. 
    Note that geographical classification here should be generalized to countrywise rather than specific lattitude/longitude point on the lobe.
    

## Description of the Dataset

  ### The size of the dataset 
       
       The dataset contains 1059 rows representing music tracks and 70 columns. Of the 70 columns, 68 represent features of music, and 2 represent lattitude and longitude, the geographical origin of the music track. 
       
       The size of the dataset is 678KB
  
       
  
  ### The types of the data 
       
       The type of the data is 
       - float with 6 digits of precision for all music features and 
       - float with 2 digits of precision for lattitude and longitude.
  
  
  
  ### Identify the features and the target (if applicable)

      Or dataset contains 68 features. We can eliminate features that do not help us solve the problem of identifying the origin of music. 
      - We can eliminate features shared by all, if any, as this does not help with narrowing our selection.
      - We can eliminate sparse data.
      - Choose features that are most relevant to the problem.

      

  ### Summary statistics of the data
        
       Calculate Mean value of each feature for each location/Country.


  ### Distribution of the target class (if applicable) and a few key features

      Target class distribution should be the same as for training set.


## Proposed Solution

    As we can bucket features into difference geospatial locations, we can solve this problem of choosing the origin of music, by using the Classification Algorithm.
    All learning has to be supervised learning, because of the nature of data we are dealing with.


## Benchmark Model

    We can compute a mean for each feature for each geographic location/Country and use this as a benchmark.


## Performance Metric

        
