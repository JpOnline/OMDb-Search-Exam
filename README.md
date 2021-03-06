# iLabSinc Exam done by João Paulo Soares

## Overview
The library [Polymer 2.0](https://www.polymer-project.org/) was used to create Web Components.

Besides what is descript in Task Details you can see these characteristics:
- Responsive Design for desktop and mobile;
- a fallback image when movies don't have poster;
- pagination over the movie results and;
- an error page when in a wrong url.

## To run the project

Note that Node.js version 6.x or 7.x and npm is required.

```bash
npm install
npm run polymer serve -o --open-path /
```

## Todo
- Indicate in the interface when data is being loaded;
- Add a logo image;
- Create service worker to show an error page indicating that the user is offline;
- Load different size images depending on user device and;
- Create a manifest to deliver the page as a Progressive Web App.

# OMDb-Search-Exam
Search the OMDb API

## Task Details
- Consume the [OMDb API](http://www.omdbapi.com/) to fetch the top 10 results matching your search query (JSON).
- Create an interface with at least one input field to be used to search for movies by title.
- Present the results in real time and update the interface as the user types his search query.
- Once the results are displayed allow the user to click on any particular movie to view its details.
- On the movie details view display the plot and other information including the poster image.
- Make your code and UI as clean as possible, be creative.
- *You have five business days from the moment you received the email linking to this repository to complete your task.*

## Requirements
- You can fork this repo or make your own.
- Please use ES6, Typescript or ES5. *No CoffeeScript*.
- You must create a SPA.
- You can use any version of Angular, React or [Vue](https://vuejs.org/) (alternatively any framework you are most comfortable with).
- You can include a `package.json` or other build tools and processors (Webpack, Babel, SASS tools, etc.).
- You can use any CSS framework or make your own styles.
- Please provide any install or runtime instructions in the `readme.md`.

## OMDb API Examples
Please note that the OMDb API does not require any form of authentication. See the [OMDb API documentation](http://www.omdbapi.com/#parameters) for all supported parameters.

### Search by query

```
http://www.omdbapi.com/?s=ghost //results 1-10
http://www.omdbapi.com/?s=ghost&page=2 //  results 11-20
```
- Returns the first 10 results based on the query value provided as `s`
- Pagination can be added via `&page=n`, where `n` is 1-100

#### Movie Object Structure
```json
{
    "Title": "Mission: Impossible - Ghost Protocol",
    "Year": "2011",
    "imdbID": "tt1229238",
    "Type": "movie",
    "Poster": "https://images-na.ssl-images-amazon.com/images/M/MV5BMTY4MTUxMjQ5OV5BMl5BanBnXkFtZTcwNTUyMzg5Ng@@._V1_SX300.jpg"
}
```

### View movie details by `imdbID`
```
http://www.omdbapi.com/?i=tt1229238
```
- Using the `imdbID` provided by the search results will let you fetch the details of a particular movie.
