# DreamWorks-Disney-or-Pixar

## Under Construction...

## Introduction
This is a repository for the “DreamWorks, Disney, or Pixar” project.


## Data and Methods 
The web-scraping was done using Python. Data manipulation and modeling were done in R. The data visualizations were made using HTML, CSS, and D3js.

<details>
<summary><b> Python Modules and Libraries: </b></summary>
  
* pandas 
* BeautifulSoup
* requests
* lxml.html 
* requests_html 
* scrapy 
* selenium
* pprint 
* itertools
  
 </details>

 <details>
<summary><b> R packages:</b></summary>
  
* reticulate
* data.table
* tidyverse
* textdata
* topicmodels
* gridExtra
*  ggplot2
  
 </details>


 <details>
 
<summary><b> Javascript libraries: </b></summary>
  
* D3.js 
* ScrollMagic
  
 </details>


Here is where you can find all of the data (**Note:** some movies were not included because certain of missing information): 

`all_movie_data.csv`:  Data set of all DreamWorks, Disney Animation, and Pixar movies.

`all_movies_tidy.csv`: Data set of all studio movies but with each tokenized word from the plot variable having its own row. 
Here are all of the words that were combined with stop words (words that are not useful for sentiment analysis:

```
custom_stop_words <- tribble(
  "shrek", "CUSTOM",
  "woody", "CUSTOM",
  "po", "CUSTOM",
  "hiccup", "CUSTOM",
  "mcqueen", "CUSTOM",
    "fiona", "CUSTOM",
  "toothless", "CUSTOM",
  "buzz", "CUSTOM",
    "puss", "CUSTOM",
  "ralph", "CUSTOM",
    "fiona", "CUSTOM",
  "elsa", "CUSTOM",
  "sulley", "CUSTOM",
    "alex", "CUSTOM",
  "mcqueen", "CUSTOM",
    "fiona", "CUSTOM",
  "dory", "CUSTOM",
  "anna", "CUSTOM",
    "bolt", "CUSTOM",
  "mike", "CUSTOM",
    "arlo", "CUSTOM",
  "marlin", "CUSTOM",
  "boov", "CUSTOM",
    "grug", "CUSTOM",
  "oscar", "CUSTOM",
    "lewis", "CUSTOM",
  "vanellope", "CUSTOM",
  "megamind", "CUSTOM",
  "andy's", "CUSTOM",
  "nemo", "CUSTOM",
  "jack", "CUSTOM",
  "andy", "CUSTOM",
  "eep", "CUSTOM",
  "peabody","CUSTOM",
  "harold", "CUSTOM",
  "tim", "CUSTOM",
  "turbo", "CUSTOM",
  "carl","CUSTOM",
  "mater", "CUSTOM",
  "merida", "CUSTOM",
  "remy", "CUSTOM",
  "sherman", "CUSTOM",
  "rapunzel", "CUSTOM",
  "miguel", "CUSTOM",
  "barry", "CUSTOM",
  "marty", "CUSTOM",
  "raya", "CUSTOM",
  "spot", "CUSTOM",
  "croods", "CUSTOM",
  "shifu", "CUSTOM",
  "tip", "CUSTOM",
  "hiro", "CUSTOM",
  "rj", "CUSTOM",
  "judy", "CUSTOM",
  "maui", "CUSTOM",
  "te", "CUSTOM",
  "cruz", "CUSTOM",
  "eve", "CUSTOM",
  "berk", "CUSTOM",
  "kai", "CUSTOM",
  "hã", "CUSTOM",
  "ian", "CUSTOM",
  "astrid", "CUSTOM",
  "shen", "CUSTOM",
  "flik", "CUSTOM",
  "bala", "CUSTOM",
  "dave", "CUSTOM",
  "drago", "CUSTOM",
  "gorg", "CUSTOM",
  "arty", "CUSTOM",
  "lenny", "CUSTOM",
  "dr",  "CUSTOM",
  "moana", "CUSTOM",
  "oogway", "CUSTOM",
  "penny", "CUSTOM",
  "roddy", "CUSTOM",
  "ted", "CUSTOM",
  "yi", "CUSTOM",
  "namaari", "CUSTOM",
  "sisu", "CUSTOM",
  "elanor", "CUSTOM",
  "jessie", "CUSTOM",
  "linguini", "CUSTOM",
  "lotso", "CUSTOM",
  "russell", "CUSTOM",
  "burnish", "CUSTOM",
  "george", "CUSTOM",
  "gloria", "CUSTOM",
  "humpty", "CUSTOM",
  "krupp", "CUSTOM",
  "li", "CUSTOM",
  "melman", "CUSTOM",
  "metro", "CUSTOM",
  "rita", "CUSTOM",
  "felix", "CUSTOM",
  "gothel", "CUSTOM",
  "mittens", "CUSTOM",
  "forky", "CUSTOM",
  "hopper", "CUSTOM",
  "grimmel", "CUSTOM",
  "aladar", "CUSTOM",
  "druun", "CUSTOM",
  "hans", "CUSTOM",
  "bo","CUSTOM",
  "boo", "CUSTOM",
  "ctor", "CUSTOM",
  "finn", "CUSTOM",
  "riley", "CUSTOM",
  "bewilderbeast", "CUSTOM",
  "fu", "CUSTOM",
  "kung", "CUSTOM",
  "rumpel", "CUSTOM",
  "baymax","CUSTOM",
  "vincent", "CUSTOM",
  "nick", "CUSTOM", 
  "donkey", "CUSTOM", 
  "bob", "CUSTOM", 
  "sugar", "CUSTOM",
  "guy", "CUSTOM",
  "baby", "CUSTOM",
  "wilbur", "CUSTOM", 
  "arendelle", "CUSTOM",
  "eugene", "CUSTOM",
  "barley", "CUSTOM", 
    "olaf", "CUSTOM",
  "everest", "CUSTOM", 
    "scanner", "CUSTOM", 
   "chicken", "CUSTOM",
  "fiti" , "CUSTOM",
  "callaghan", "CUSTOM",
    "kron", "CUSTOM",
    "gem", "CUSTOM",
  "fury", "CUSTOM",
  "dragon", "CUSTOM",
  "ants", "CUSTOM",
  "cy", "CUSTOM",
    "doris", "CUSTOM",
  "goob", "CUSTOM",
      "scanner", "CUSTOM",
    "calhoun", "CUSTOM",
  "dragons", "CUSTOM",
  "penguins", "CUSTOM",
  "toys", "CUSTOM",
  "toy", "CUSTOM",
  "rush", "CUSTOM",
  "game", "CUSTOM",
  "kristoff",  "CUSTOM",
  "bonnie",  "CUSTOM",
  "elinor",  "CUSTOM"

```

`all_movie_sentiment_afinn.csv`: Data set of overall studio positivity and negativity scores based on the AFINN dictionary. 

`all_movie_sentiment_bing.csv`: Data set of overall studio positivity and negativity scores based on the bind dictionary. 

`all_movie_topics.csv`: Data set of all of the plot variable words with the probability (beta) that they belong to a particular topic (topic). 

`Animation_company_data.csv`: Data set of the average value of finance, reception, and impact metrics for each studio. 

The sentiment analysis performed for this project was aimed at determining how positive or negative the language used to describe the movie plots was. This process involved 4 steps: stripping the plot summary data into single words, removing inconsequential words (names, articles, prepositions, etc), joining the words with dictionaries/lexicon that have labeled the valence of our keywords, and calculating the overall sentiment for each studio.


Topic modeling uses a statistical model to uncover abstract topics from textual data. The framework I specifically used was Latent Dirichlet Allocation (LDA) and it involved: taking the studio grouped keywords from the earlier data preparation, generating a document term matrix, and using that matrix to generate the probabilities that each word is associated with a particular topic.

Because there is a large amount of subjectivity with determining how many topics should be generated, how many words should be cut out, and how many high-frequency words should be shown, all of the data used at differing steps will be made available via my GitHub. This exploratory analysis showcases what I thought was relevant. LDA forces us to have at least 2 topics, but from what I found, the words associated with the second topic were not similar enough to derive a clear theme. So I will only be displaying one topic for each studio.



## Sources
[Pixar Animation Studio](https://en.wikipedia.org/wiki/Pixar): The studio level Wikipedia data was gathered on this page. 
[Pixar Movie List](https://en.wikipedia.org/wiki/List_of_Pixar_films): Go to this page for Pixar movie data.

[Disney Animation Studio](https://en.wikipedia.org/wiki/Walt_Disney_Animation_Studios): The studio level Wikipedia data was gathered on this page. 
[Disney Movie List](https://en.wikipedia.org/wiki/List_of_Walt_Disney_Animation_Studios_films): Go to this page for Disney movie data.


[DreamWorks Animation Studio](https://en.wikipedia.org/wiki/DreamWorks_Animation): The studio level Wikipedia data was gathered on this page.
[DreamWorks Movie List](https://en.wikipedia.org/wiki/List_of_DreamWorks_Animation_productions): Go to this page for DreamWorks movie data.


[IMDB Web-scraped Data](https://www.kaggle.com/stefanoleone992/datasets): The IMDB web-scraped data was gathered by this user. But the page for the dataset no longer exists. 



## Contact Me

|**Contact Method**  |                          |
| -------------------| -------------------------|
| Professional Email | cedric.lary1@gmail.com   |

