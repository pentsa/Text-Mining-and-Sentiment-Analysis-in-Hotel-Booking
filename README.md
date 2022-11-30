# Text-Mining-and-Sentiment-Analysis-in-Hotel-Booking

## Introduction 
Hotel reviews become one of the important factors that people consider when making hotel bookings. However, the customer reviews were often not fully utilised and considered when planning marketing campaigns. Therefore, this study aims to discover the terms in the reviews that are meaningful to reflect customer’s feedback that can potential affect hotel’s booking rate. Using R studio, data from "Hotel customer reviews" was retrived and organised for further analysis. The term frequency matrix was analysed and presented with no significant meanings. When scanning across multiple documents, term frequency alone provided an incomplete analysis of the true importance of a given word. Therefore, the study continued by combining term frequency with inverse document frequency to provide ingihts relating to the important terms in the reviews. The terms with the highest collective importance using Term Frequency - Inverse Document Frequency were “great”, “nice”, “clean”, and “good”. This insight can be considered when utilising customer reviews as marketing campaigns for hotels to raise the hotel booking rates. Further study can be conducted to discover the correlation between hotel ranking and term freqeuncy in the customer reviews with larger dataset to provide more detailed insights. 

## Features
- Data cleaning was performed to generate structured data
- Data Summary 
- Term freqeuncy matrix analysis 
- TF-IDF (Term frequency – inverse document frequency) matrix analysis 

## Content 
- Dataset Retrieval 
  -  The data from "..." was utilised for further text minning 
- Data cleaning 
  -  Package (stringi) was installed to faciliate text strings processing
  -  stri_encode and stri_enc_mark functions were applied to convert string between encode.
- data summary 
  - sapply function was applied to calculate the word length of  review. The mean was found to be 124.7
  - ggplot function was applied to present the word length of reviews in histogram
  - <img width="650" alt="截圖 2022-11-25 下午2 25 17" src="https://user-images.githubusercontent.com/117743186/203914660-28b5435b-5044-483f-ab0e-6eb492715064.png">

- Text freqeuncy matrix analysis 
  -  the textcat package was installed to generate a list of english reviews for text mining 
  -  the tm and SnowballCwas packages were also installed to generate reviews 
  -  VCorpus function was applied to create volatile corpora, followed by tm_map function for further processing to clean up the corpora
  -  The final term-document matrix was created using DocumentTermMatrix function 
  -  The slam package was utilised to displays TF of terms in descending order
  -  <img width="583" alt="截圖 2022-11-25 下午2 25 44" src="https://user-images.githubusercontent.com/117743186/203914737-e2acfb5b-6a93-49f5-9b09-81009d4dbd25.png">
 -  TF-IDF (Term frequency – inverse document frequency) matrix analysis
  -  weightTfIdf function was utilised to create TF-IDF matrix, followed by presentation of the matrix using sort function
  -  <img width="613" alt="截圖 2022-11-25 下午2 26 17" src="https://user-images.githubusercontent.com/117743186/203914798-95a85b4e-6b60-4a45-8ea7-7d7ba33d450c.png">

## Key findings
1. Words like “great”, “nice”, “clean”, and “good” have a higher value on the TF-IDF than the TF matrix, which are much more helpful terms than “hotel”, “room”, “stay”, and “staff”, when trying to summarize whether reviews were generally positive or negative.
