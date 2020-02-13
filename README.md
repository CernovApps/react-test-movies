# React Test: Movies

## Overview
This is a test about react.js, web development and/or javascript skills. This is not a closed problem, but an opportunity to show us your skills, primarly (but not exclusive) creativity, problem design, agile, scalable and bug free development.

## Instructions
You're gonna to start from a existing react app project and are going to work on top of it, modifying according to your client needs (in this case, us). The project can be cloned from 

    http://react-movie-cards.drminnaar.me/ 
    
(you can follow its Getting started to setup and run it). 

After setupping and running this template locally, it should be something like showed here:

    https://github.com/drminnaar/react-movie-cards.
    
If you have any troubles, you can ask for help (or search by yourself, but be careful of Hero Sindrome).

### Task 1
In this task you'll need to populate the main view (cards grid list) with movies data from a REST API.

#### Part A
##### First
Access and explore, if you want to, this link: 

    https://www.themoviedb.org/ 
    
and familiarize with its services.

##### Second
Choose some method to get movie data from it. We suggest something like this end point: 

    https://developers.themoviedb.org/3/discover/movie-discover
    
but you are free to choose any other will want.

##### Third
Make a requisition from your app and organize the data you will need to use in your app later.

##### Tips / extra explanation

You can use this api key:

    87dfa1c669eea853da609d4968d294be

or get your own.

There is already a service to get movie data, but it's getting from a json file. In terms of integration and better organization, try to modify the file MovieService.js to make all requisitions and make data accessible.


#### Part B
In this part you're gonna to integrate your fetched data!
If you've used the suggested route, the movie data will come as something like this (something inside answer object):

    {
          "popularity": 389.165,
          "vote_count": 2281,
          "video": false,
          "poster_path": "/xBHvZcjRiWyobQ9kxBhO6B2dtRI.jpg",
          "id": 419704,
          "adult": false,
          "backdrop_path": "/5BwqwxMEjeFtdknRV792Svo0K1v.jpg",
          "original_language": "en",
          "original_title": "Ad Astra",
          "genre_ids": [
            12,
            18,
            9648,
            878,
            53
          ],
          "title": "Ad Astra",
          "vote_average": 6,
          "overview": "The near future, a time when both hope and hardships drive humanity to look to the stars and beyond. While a mysterious phenomenon menaces to destroy life on planet Earth, astronaut Roy McBride undertakes a mission across the immensity of space and its many perils to uncover the truth about a lost expedition that decades before boldly faced emptiness and silence in search of the unknown.",
          "release_date": "2019-09-17"
    },

You'll have to provide to card and show, replacing original data type but keeping its style, the following parameters from your fetched data for each movie:

    imageUrl -> Use backdrop_path (with base url http://image.tmdb.org/t/p/original) provided form api instead of local images
    title -> Use title provided from api
    subtitle -> Replace it to release_date, properly showed as DD/MM/YYYY, but keeping its style
    description -> Use overview provided from api


### Task 2
In this task you will need to modify some style from components. Apply the following changes:

- Center the cards inside main view (cards grid list) (it's originally in flex-start / left)
- Change the avaliation chip (blue chip with a white number inside of each card) to align with the stars, it should be vertically centered.


### Task 3
Make a like button in each card that should notify if you have already reacted to that movie. Don't worry to much about the design aspect. You could implement something like this:

    https://storage.googleapis.com/spec-host/mio-staging%2Fmio-components%2F1579302979877%2Fassets%2F1eZNTdj8h1J0BFkbl23LyzEwjjvMzY_uV%2Fcards-elements-2b.png


In this moment do not worry about storing this data, but feel free to implement in this way if you want (this is kind of a bonus).
