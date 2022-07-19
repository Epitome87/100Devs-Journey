# Class 40 - MongoDB

## Agenda

- Review: CRUD
- Review: Express
- Learn: Post & Delete
- Learn: Build Your App
- Homework: Build Your Own App

## MongoDB

A database. If you've ever used objects, you can easily use MongoDB.

Collection and Documents.
Collection: Made up of individual documents.
Documents: An Object.

No querying language to learn!
Can use Mongo Atlas to use a cloud database.

## EJS

Embedded JavaScript Templates

```js
<ul class="rappers">
<% for (let i = 0; i < info.length; i++) {%>
    <li class="rapper">
        <span><%= info[i].stageName %></span>
        <span><%= info[i].birthName %></span>
    </li>
<% } %>
</ul>
```

Blocks of code go between `<% %>`
Variables go between `<%= %>`

## MongoDB

A high-level overview of MongoDB was provided, but nothing worth taking notes on.

## Homework

- Create: Heroku, Mongo Atlas, and Postman Accounts
- Read: https://zellwk.com/blog/crud-express/mongodb
- Do: Make Your Own App and Push to Heroku
