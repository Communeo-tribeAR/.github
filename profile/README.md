# Communeo Películas Tribe ARGENTINA (AR)

This project is movie library where list of movies are displayed. It is simply showcase of angular features such as modules, components, services, routing, data-binding, etc.

### [Demo](https://Communeo-app-29a50.firebaseapp.com)

## Prerequisites

**BEFORE YOU RUN:** Install Angular CLI
```bash
npm install -g @angular/cli
```

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

![screen shot 2017-09-02 at 9 39 08 pm](https://user-images.githubusercontent.com/9882972/29997031-3a935ca8-9027-11e7-9671-ab37a064b4b0.png)

The internet movie database, [imdb.com](http://imdb.com/), is a website devoted to collecting movie data supplied by studios and fan.  It claims to be the biggest movie database on the web and is run by amazon.  More about information imdb.com can be found [online](http://imdb.com/help/show_leaf?about), including information about the [data collection process](http://imdb.com/help/show_leaf?infosource).

IMDB makes their [raw data available](http://uk.imdb.com/interfaces/). Unfortunately, the data is divided into many text files and the format of each file differs slightly.  To create one data file containing all the desired information these ruby scripts extract the relevant information and store in a database.  Finally, this data is exported to csv to make it easier to import into data analysis packages.

The following text files were downloaded and used:

* business.list. Total budget
* genres.list.  Genres that a movie belongs to (eg. comedy and action)
* movies.list.  Master list of all movie titles with year of production.
* mpaa-ratings-reasons.list.  MPAA ratings.
* ratings.list.  IMDB fan ratings.
* running-times.list.  Movie length in minutes.

Movies were selected for inclusion if they had a known length and had been rated by at least one IMDB user. The final output contains the following fields:

* title.  Title of the movie.
* year.  Year of release.
* budget.  Total budget (if known) in US dollars
* length.  Length in minutes.
* rating.  Average IMDB user rating.
* votes.  Number of IMDB users who rated this movie.
* r1-10.  Distribution of votes for each rating, to mid point of nearest decile: 0 = no votes, 4.5 = 1-9$\%$ votes, 14.5 = 11-19$\%$ of votes, etc.  Due to rounding errors these may not sum to 100.
* mpaa.  MPAA rating.
* action, animation, comedy, drama, documentary, romance, short.  Binary variables representing if movie was classified as belonging to that genre.
