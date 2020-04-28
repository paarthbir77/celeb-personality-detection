# celeb-personality-detection
 Problem Statement : Crawl popular websites & create a database of Indian movie celebrities with their images and personality traits.
The project aims to crawl google news search results for 10 Indian celebrities and use the urls found from scraping the search result to further scrape data about the celebrities including relevant textual data and images. The notebook celeb info extractor.inpyb can be run to create a database of images and textual data. personality.ipynb gives the model predictions for the celebrity MBTI based on the text scraped.
### Project Structure (prior to running celeb info extractor):
-root folder
-- textfiles/
-- celebrities/
-- datasets/
-- celeb info extractor.ipynb
-- personality.ipynb
-- personality test code.ipynb
### Dataset
For personality detection from the extracted text data the Kaggle MBTI dataset (Around 8600 posts) and the Reddit MBTI dataset (Around 9300 posts) were used.
Dataset Distribution:
After removing null data points, 16140 training instances and 1798 validation instances were taken with the distribution for classes:

training distribution:                         validation distribution :

infj     1820                                     infj    217
infp     1760                                     intj    192
intj     1562                                     intp    165
intp     1265                                     infp    162
entp     1073                                     entj    128
enfp     1023                                     entp    119
istp     1005                                     istp    112
entj     1000                                     isfp    110
isfp      996                                     enfp    109
istj      962                                     isfj    102
enfj      945                                     istj     97
isfj      915                                     enfj     87
estp      590                                     estp     64
esfp      495                                     estj     50
estj      399                                     esfj     49
esfj      330                                     esfp     35


### To-Do:
1. At present the code uses google search url, to automate the process such that it does not require google search url
2. To improve the NLP model, current model provides a training accuracy of 87.5% and a validation accuracy of ~63.2% clearly overfitting. New architectures to be considered.
3. Address the class imbalance, can be done with class weights in loss function.
### Libraries used:
1. Beautiful Soup, requests, urllib for scraping
2. regex for text processing
3. pandas, numpy for dataset handling
4. Tensorflow/Keras for NLP
