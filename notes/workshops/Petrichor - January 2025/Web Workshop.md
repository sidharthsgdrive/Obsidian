DOM - Document Object Model (structure that we see when in inspect element)

**the role of web servers**
web servers are programs that listen for HTTP requests over the internet and reply with HTTP Reponses.

**JS and typescript**
A dynamically typed programming language used to add interactivity and responsiveness to websites
Typescipt extends JS (as a superset) by introducing static typing, TS is now the industry standard

**Use of frameworks**
frameworks treat the web as an application framework to simplify implementation of interactive features

**Modern web application architecture**
MVC (model view controller) lacks a frontend
JS-based fullstacks

**Backend in Fullstack frameworks**
We shouldn't expose backend code to the end user. Thus, we should have a place to store code in the server.
+page.server.ts file is responsible for loading the data and handling forms, server.ts endpoints exist to deal with loading data at arbitrary time.
+page.ts runs on the client side.

**Databases**
* SQL (structured) requires you to use predefined schema before entering data
* NoSQL (non-structured) has a dynamic schema for unstructured data

**ORM**
Object-Relational Mapping is a technique that lets you query and manipulate data from a database using an OO paradigm. We can use an object to manipulate a database.
The benefit is that we don't need to use SQL commands, which are strings and potentially breakable.

**Drizzle - the TS ORM**
Its the only ORM with both relational and SQL-like query APIs

SQLite handles database deletion and resetting easily, and is thus used extensively in iterative testing, even if it's replaced by with, say, Postgres in production.

**Composition in frontend**
The main idea of many frontend flavors is to create small reusable components that we can reuse across the site.
It's common practice to create components in the lib folder and import it to the routes folder.

note: execute "pnpm dev" to start live server, --host to host the code

**Sites for hackathons**
flipr
devfolio

**Site hosting**
Render, Vercel

