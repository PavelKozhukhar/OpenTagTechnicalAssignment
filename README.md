# OpenTagTechnicalAssignment
This a repository where Pavel's Technical Assignment is present


There is provided a Postman collection with the results of my Technical Assignment. Here will be described how it works. 

In the first request I tried to do something like that:
```
query GetAllSpeciesFromTheFirstMovie {
  allFilms {
    films(title: "A New Hope") {
      id
      title
      speciesConnection {
        species {
          name
        }
      }
    }
  }
}
```
But I  have got an error: _Unknown argument \"title\" on field \"films\" of type \"FilmsConnection\"._

After that I tried something like that:
```
query GetAllSpeciesFromTheFirstMovie {
  allFilms {
    films(filter: {
      "title": "A New Hope"
      }) {
      id
      title
      speciesConnection {
        species {
          name
        }
      }
    }
  }
}
```

But I have got an error: _Unknown argument \"filter\" on field \"films\" of type \"FilmsConnection\"._
From what I could understand - for these filters to work - it needs to be written in the schemes, but this was not done in this sandbox


It was a hard fight, I tried desperately to get this filter to work, but it was all in vain. And after that I decide to get data from the **film** table. So, first of all I get an ID of the first movie, and than use it in my request. 

Same with the second request, I was trying to apply some filters, but it was not successful, and I went the same way, finding the ID of the needed person, and after that getting the data about it.

My third task was to get some data about all peoples in the movie. It was not clear, should I filter data by the specific part of the movie or just by all films. Taking into account my problems with the filters -- I just get this needed data by all movies.

And same in the last task, the filter still didn't work as I want to, and because of it I found a specific person in the last request, and just get data about it. I hope that I choose a right person. In the task there was "person with unique id = 4", but I don't found numeric ID of the person and just get the forth person in the last request. 

I hope I was right about these filters, and they really don't work here(but can work if it will be implemented by developers), and I did all tasks in the right way =)
