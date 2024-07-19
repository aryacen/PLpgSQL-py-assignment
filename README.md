# Movie Database Queries

## Overview
This project consists of a series of Python scripts that interact with a movie database using PLpgSQL. Each script performs specific queries to retrieve and display information about movies, directors, genres, and roles. This assignment was awarded a 100% mark, reflecting its completeness and accuracy.

## Exercises

### Q1: The dirby (Directed By) script (3 marks)
Complete the Python3 `dirby` script that takes one command-line argument, the name of a person, and prints:

- a list of films that this person directed, or
- a message that the person didn't direct any films, or
- a message that the person does not exist in the database

Note that there are some names that occur multiple times. Choose only people who have worked as directors, and then choose the first one from that list ordered by People.id. If none of the matching people are directors, exit with the message "None of the people called Name has directed any films".

Examples of using the script can be found on the Examples page.

### Q2: The releases script (4 marks)
Complete the Python3 `releases` script, that takes two command-line arguments, the complete title of a movie and the year it was made, and lists all of the countries where it was released. The movie title must be an exact match to the title in the database (the words, the punctuation, and the capitalization). If the title contains multiple words, you will need to put them in quotes on the command line (e.g. "Bad Influence"). The year must be a four-digit string (e.g. 2012).

You can assume that the combination (title, year) is unique, even though there are some counter-examples in the database. We will not test any cases where (title, year) is not unique.

First, check that the year is valid (i.e. four digits). If not, exit with the message "Invalid year".

If the movie does not exist in the database, print the message "No such movie", and exit the program. If the movie does exist, but has no releases mentioned in the database, print the message "No releases" and exit the program. Otherwise, print a list of country names, one per line, in alphabetical order, for all of the countries where the movie was released.

Examples of using the script can be found on the Examples page.

### Q3: The genres script (3 marks)
Complete the Python3 `genres` script, that takes one command-line argument, a year, and prints a list of the top-10 genres of movies released during that year. Order the list in descending order based on the number of movies in each genre. For genres that have equal numbers of movies, order by the genre names.

First, check that the year is valid (i.e. four digits). If not, exit with the message "Invalid year". If there are no movies in the given valid year, exit with the message "No movies".

## Q4: The roles script (4 marks)
Complete the Python3 `roles` script, that takes a single command-line argument, the name of an actor/actress, and prints a list of the roles they played. (Note: treat a principal whose job is self the same as an actor/actress.) Each entry in the list gives the name of the character and the title and year of the movie it's in. The list should be ordered by year, then by movie title, then by role name.

If the name does not exist in the database, then print the message "No such person". If the person had no acting roles, then print the message "No acting roles".

There are instances where several people have the same name. In these cases, it should print a list for each person, introduced by their name and a number. If only one person has the name, we simply print the role list without name or number. Order the list of people by their People.id.

Examples of using the script can be found on the Examples page.

## Q5: The movie script (6 marks)
Complete the Python3 `movie` script, that takes a single command-line argument, the (partial) name of a movie, and prints a list of all the principals in the movie. Order this list based on the ordering given in Principals.ord.

Actors and actresses should have the role they played in the movie next to their name; if there is no role information for that person, display "???" as the role. Treat principals with the job self the same as actors/actresses. Other principals should display their name and the job they performed (e.g. director, cinematographer).

If more than one movie matches the partial title, display a numbered list, ordered by title, then year, of matching movies, followed by a prompt to select one movie (by its number). Then display information about that particular movie as described above.
