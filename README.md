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

### Example 5: a ```/books``` request

<img width="329" alt="Снимок экрана 2022-10-05 в 2 31 43 PM" src="https://user-images.githubusercontent.com/103382741/194050707-1cdd19c1-f7e9-4e72-af45-7e50b5f0a870.png">

So here we have list of books, that we currently have in our library. There is shown some information about them: Name, Author, Year (of publishing). You can also see a button that allows you to add a new book to this list and a button that directs you to the list of readers (example 1). Each line is a link to the page, where you can see more specific info about the book you've chosen (example 6)

### Example 6: a ```/books/{id}``` request

<img width="369" alt="Снимок экрана 2022-10-05 в 2 44 03 PM" src="https://user-images.githubusercontent.com/103382741/194052703-e0e7d648-7d4d-4607-ac30-7e7bdeaf936d.png">

On this page we can see again the info about the book and also it's shown if the book is free or there is who took it (see below). If it's free we can assign it to someone from the list of readers by choosing the person in the list:

<img width="361" alt="Снимок экрана 2022-10-05 в 2 47 18 PM" src="https://user-images.githubusercontent.com/103382741/194053272-4a84730b-b619-4035-af40-407ee3139de1.png">

When we are ready with our choice we click on the person and then click on the button "Assign book"

<img width="300" alt="Снимок экрана 2022-10-05 в 2 48 40 PM" src="https://user-images.githubusercontent.com/103382741/194053508-c5095177-a57b-45fc-8664-ac870d2ce033.png">

When it's done we can see this page, where it's said who has taken this book and by clicking 
the button "Release" we can make it free again!

And if we have a desire we can remove this book from the list.

### Example 7: a ```/books/{id}/edit``` request

<img width="263" alt="Снимок экрана 2022-10-05 в 2 51 11 PM" src="https://user-images.githubusercontent.com/103382741/194053926-3c4267ae-5339-46c6-bab0-94465f7770d3.png">

Here we have almost the same page of editing as we had for people (example 3) with same validation. After finishing your update you click the button "Update" and new data will be added.
