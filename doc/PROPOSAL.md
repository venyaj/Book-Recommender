# Book Recommendation System

## Overview

In our project, we will create a system to recommend books to users. The user should enter their book ratings. From there, they can either allow an algorithm to pick recommendations for them, or customize several options, such as sorting/filtering by book length, minimum average rating, genre, author, etc. The datasets we plan to use come from Kaggle:

https://www.kaggle.com/arashnic/book-recommendation-dataset

https://www.kaggle.com/choobani/goodread-authors

## Usefulness

While Goodreads already has a similar purpose, our system could have more customization options. This would allow users to get recommendations that more closely fit their tastes. Also, other databases like https://www.whatshouldireadnext.com/ require you to type in a single book, whereas our system will use will use multiple factors such as a user's rating, and what other users with similar purchase lists liked. 

## Functionality

Our database will store information for each book including ISBN, book name, genre, publisher, language, year published, author, rating, and even the front cover of the book. We will also store (User, Book, Recommendation) triplets. Through our website, users can sign up and enter their own recommendations into the database (would require storing personal information). By entering information like books they've read in the past and ratings, we can personalize recommendations to find books with suitable language, similar series and so on. Users can also search for books by keyword, and update or delete their recommendations. We would probably use stored procedures to generate algorithmic recommendations. We could add a quiz to determine users' preferences as an additional interesting feature, instead of needing to enter recommendations or features manually.

## Low fidelity UI mockup
See doc/mockup.pdf

## Work distribution

Our group will meet weekly to discuss overall progress. We can meet on Friday afternoon around 3 PM.

Zoom link:
Join Zoom Meeting
https://illinois.zoom.us/j/84207067230?pwd=cktLNGpQenRHdDRNUi8waXcvNTNxUT09

Meeting ID: 842 0706 7230
Password: 241540

Making database and loading data - Tommaso

Creating server's stored procedures- Venya

Interfacing with Web client - Chahna

Recommendations - Dio

If anyone needs help on one specific part, we can take a look at it with the whole group.


