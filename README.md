# Ironhack Project Case Study - GNOD 🎼 🎧 🎙️
by [Josephine Biedermann](https://github.com/JosephineBiedermann), May 2021

## Building a tool that recommends a song to the user based on the users input.
  
  
## Table of content

- [Project Brief](https://github.com/JosephineBiedermann/Week7Project/blob/main/README.md#project-brief)
- [Process & Tools](https://github.com/JosephineBiedermann/Week7Project/blob/main/README.md#process--tools)

## Project Brief
**Scenario:**
Gnod is a site that provides recommendations for music, art, literature and products based on collaborative filtering algorithms. 
Their flagship product is the music recommender, which you can try at www.gnoosic.com. The site asks users to input 3 bands they like, and computes similarity scores with the rest of the users. Then, they recommend to the user bands that users with similar tastes have picked.

**Challenge:**
We are trying to come up with ways to enhance our music recommendations. One of the new features we'd like to research is to recommend songs (not only bands). We're also aware of the limitations of our collaborative filtering algorithms, and would like to give users two new possibilities when searching for recommendations:
- Songs that are actually similar to the ones they picked from an acoustic point of view.
- Songs that are popular around the world right now, independently from their tastes.

**Tasks:**
- explore new data sources for songs: collect as much information as possible from popular songs
- collect data (few hundreds or thousand) from each source and see if the collected features are useful
- create clusters of songs that are similar to each other. The idea is that if a user inputs a song from one group, we'll prioritize giving them recommendations of songs from that same group.
- present work

## Process
- Data gathering 1 - webscraping hot100 bilboards - [notebook](https://github.com/JosephineBiedermann/Week7Project/blob/main/code/LAB_Webscraping.ipynb) - [data](https://github.com/JosephineBiedermann/Week7Project/blob/main/data/top_100_songs.csv)
- building prototype 1 - [notebook](https://github.com/JosephineBiedermann/Week7Project/blob/main/code/LAB_Recommendation_function.ipynb)
  In the first prototype we are requesting a song from the user and test if this song is in the hot100 database we scraped from the billboard webside.
  If the song is in the database we are recommending another random song from the hot100 database.
  The prototype can take missspelled input songs and check if there was an invalid entry.
![1st prototype](https://github.com/JosephineBiedermann/Week7Project/blob/main/images/1st_prototype.jpg?raw=true)
- data gathering 2 - using Spotipy API to get more songs for comparison - [notebook](https://github.com/JosephineBiedermann/Week7Project/blob/main/code/LAB_API_Wrapper_cleaned.ipynb)
- building kmeans model for clustering of gathered songs - [notebook](https://github.com/JosephineBiedermann/Week7Project/blob/main/code/LAB_KMeans_latin.ipynb) - [data](https://github.com/JosephineBiedermann/Week7Project/blob/main/data/audiofeatures_latin_playlists_merged.csv) 
- building prototype 2
![2nd prototype](https://github.com/JosephineBiedermann/Week7Project/blob/main/images/2nd_prototype.png?raw=true)
- putting prototype 1 and 2 together to the final tool



## Sources (not complete)
- [Spotipy Library ](https://developer.spotify.com/documentation/web-api/reference/#category-search)
#  
**Thank you for reading!** <br/>
If you have any questions, please reach out.
