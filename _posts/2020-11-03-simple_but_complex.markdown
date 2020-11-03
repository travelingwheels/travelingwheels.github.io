---
layout: post
title:      "Simple but complex"
date:       2020-11-03 22:57:29 +0000
permalink:  simple_but_complex
---

This project is a "simple" one page application, but it is also complex.  I set up both a back-end and a front-end repository. The back-end utilizes rails as an API and the front-end uses HTML/CSS/Javascript.

I used the Rails generator to set up the API. This generator will Skip generation of view files and slim-down the middleware. Also I used postgres as  the database for this project.
```
$ rails new Movies-Backend --api --database=postgresql
```
Some of the complexity started when trying to connect the front-end to the back-end. Defining params in the back-end and setting up controller actions to match the way the data comes in from the front-end through JSON. JSON is the go between, it converts the data coming from the front-end to a format the back-end can understand and vice versa.

On the front-end I used get and post fetch requests, then manipulated the DOM with the data received from the back-end.

```
function postFetch(title, description, image_url, category_id) {
    fetch(endPoint, {
        method: "POST",
        headers: {"Content-Type": "application/json",
                  "Accept": "application/json"
                },
         body: JSON.stringify({
            title: title,
            description: description,
            image_url: image_url,
            category_id: category_id
        })
    })
        .then(res => res.json())
        .then(movie => {
            const newMovie = movie.data
            let movieData = new Movie(newMovie, newMovie.attributes)
            frontendMovies.push(movieData)
            const sorted = Movie.sortByTitle(frontendMovies);
            document.querySelector('#movie-container').innerHTML = " "
            sorted.forEach(movie => {
            document.querySelector('#movie-container').innerHTML += movie.renderMovie()   
            })  
         })
         .catch(error => console.log(error));
}
```

The above snippet is my post function. In this function when I get the data from JSON I assign a variable to movie.data because of the way the data is nested. I have an empty array called fronendMovies which gets information passed to it through the Movie class. At that point I use a static sort method defined in my Movie class to arrange the HTML output in alphabetical order. In the first document.querySelector I made it equal an empty string to clear the data already displayed, then sort through the array and display the updated data. I found that if I didn't do that I would get double of everything.

I also created  a search function using the keyUp listener. I spent a lot of time Googling to figure this function out, but I am glad I did because it is the functionality that I wanted for my search feature.

If the future, I would like to make the form part of the application  modal. When you search for a title you have to scroll down to see the options and thats not good. Also I think about using a sign up and login but I'm  not convinced it is totally necessary for this application.
