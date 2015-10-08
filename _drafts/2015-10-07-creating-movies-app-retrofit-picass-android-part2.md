---
layout: post
title: Creating a Movies App using Retrofit and Picasso - Part 2
description: Using open source libraries Picasso and Retrofit to get popular movies from a REST api.
---
![alt text](/public/images/movies-app/pop-movies.gif "Popular Movies app animated image preview")

This post is part of my talk "Getting Started with Android Development" at [DEvcon](http://devcon.dominionenterprises.com/2015/){:target="_blank"}.
We will be building a movie app that consumes a REST api using retrofit and displays images using Picasso. I see this project as a "Hello World" on steroids,
so you don't need any Android experience to complete it. However, I do recommend having some programming background using Java or another Object Oriented Programming language.
In [part one](/2015/10/06/creating-movies-app-retrofit-picasso-android/), we set up the project and a grid using a mock movie poster
This is part two where we will use Retrofit
and show real movie posters as well as detail information for each movie.
<!--more-->

### Introducing the Movies Database Api
We will be using [The Movie Database Api](http://themoviedb.org){:target="_blank"} to get some real data into our app.

 	

### Creating the Rest Interface
Retrofit allows us to turn a **REST API** into a **Java interface**. This removes a lot of the boiler-plate code one would have to write to accomplish the same results without using any libraries.

Let's create our REST interface.
Create a new file called MoviesApiService.java under `app/src/main/java/com.mateo.popularmovies/`

{% highlight java lineos %}
public interface MoviesApiService {
    @GET("/movie/popular")
    void getPopularMovies(Callback<Movie.MovieResult> cb);
}
{% endhighlight %}





