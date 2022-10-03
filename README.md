# Spring Project 1

A simple virtual library implementation. It is based on Spring Boot and built with Intellij IDEA.

### About

With the advent of technology, the work of librarians seems less efficient. So let's create a special service for that! Using Spring and connecting to our local database (PostgreSQL), I showed how the library works: we add/remove people to the list of readers, we add/remove books from the library list, we assign books to readers or release them.

Keep your voice down, you're in a library!:)

## Examples
Our requests will always start with "http://localhost:8080", so let's omit this
### Example 1: a ```/people``` request

<img width="257" alt="Снимок экрана 2022-10-03 в 6 27 02 PM" src="https://user-images.githubusercontent.com/103382741/193616187-875a4f76-1822-45fc-827d-57eac39f1391.png">
So here we have a list of people (readers), that are taken from database. Each line is a link to person's profile (See example 2). After a horizontal bar you can see a button, using which you can add a person to the list of readers (See example 4). And after second horizontal bar there is a button that directs you to the books page (See example 5).

### Example 2: a ```/people/{id}``` request

<img width="333" alt="Снимок экрана 2022-10-03 в 6 33 02 PM" src="https://user-images.githubusercontent.com/103382741/193617606-3404259c-18e6-42c9-8251-67d720b3066c.png">
Here you can see info of a person you decided to see (entering his id). It also shows wheter he has taken any books or not. Lower you can see button "Edit", which directs you to the page of editing person (See example 3), and "Delete", which deletes person from the list of readers.

### Example 3: a ```/people/{id}/edit``` request

<img width="264" alt="Снимок экрана 2022-10-03 в 6 37 45 PM" src="https://user-images.githubusercontent.com/103382741/193618596-ccc7ca0c-53f0-4687-9a59-03db92079d18.png">
Here you can update personal info of a current reader and after press button "Update". It will save the changes, if they passes the check.

### Example 3.1: a ```/people/{id}/edit``` request with errors

<img width="303" alt="Снимок экрана 2022-10-03 в 6 43 45 PM" src="https://user-images.githubusercontent.com/103382741/193619959-fe737e9e-cde7-4fff-b6a6-42a5646f7fff.png">

### Example 4: a ```/people/new``` request

<img width="254" alt="Снимок экрана 2022-10-03 в 6 45 52 PM" src="https://user-images.githubusercontent.com/103382741/193620444-f41c9e52-fd7c-472b-92f3-8175cd060303.png">

Using this form you can add new reader to the list. And again you can only add person if it passes the check (as in example 3.1)
