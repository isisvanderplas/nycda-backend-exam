## NYCDA Backend Exam
=====================
Explain the questions well!!

### 1- Why do we should include script tags at the very end of an html file, before closing </body>?
  it will make the page load faster, at least easthetically, because now the computer can read all the code first and show it, instead of stopping to read the scripts first. the website will fully function once all the script tags are read, but it looks finished to the client side.

### 2 - What is a middleware?
    a middleware is a small software that you download and require, because it doesn't come with the operating system. It runs between the client and the serverside, it's been described as "glue".
    I give up.
    Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.Middleware functions can perform the following tasks:

    Execute any code.
    Make changes to the request and the response objects.
    End the request-response cycle.
    Call the next middleware function in the stack.
    If the current middleware function does not end the request-response cycle, it must call next() to pass control to the next middleware function. Otherwise, the request will be left hanging.

    An Express application can use the following types of middleware:

    Application-level middleware
    Router-level middleware
    Error-handling middleware
    Built-in middleware
    Third-party middleware
    You can load application-level and router-level middleware with an optional mount path. You can also load a series of middleware functions together, which creates a sub-stack of the middleware system at a mount point.

    I know this is copy paste, but is this the right answer?



### 3 - Why do we use express.static() middleware?
  it enables static files to be used. like pictures, or javascript or html/pug. everything that's settled, and wont change.

### 4 - What is favicon.ico ?
  the little picture you see in the tab on the left of the site name

### 5 - Why do we use a bodyParser middleware ?
  when you use POST, you need the body-parsing middleware to make the req.body readable to us, puny humans, except Izel, who is excellent.

  there are several options: raw(=>?), text(gives string), url-encoded(parses url-encoded data, only computers can read this) and json(parses to a json file) (I may have used google #shame)

### 6 - What is the difference in terms of parsing a data received from a web form with POST or an AJAX POST request?
  (I'm not sure if I understand the question, but here goes)
  AJAX will make a "live" post. it will be immediatley visible to the client side, they don't have to renew the page to see the post. eg. a chat.
  sorry I don't know!

### 7 - Why do we use methodOverride middleware ?
  sometimes the client side doesn't support our code, maybe because of an old browser. because of this middleware, the site can still be used, because it provides a fake http support.

### 8 - What are the differences between sessions and cookies ?
  session is temporary, it lasts one session (until the browser is closed), cookies will last until the client deletes them sessions are stored server side, cookies are stored client side. sessions store objects, cookies store strings

### 9 - Why do we use a session middleware ?
  to keep the client logged in, even if they renew the page. the session will end after the browser is closed. it is safer that a cookie, and the client can't read it.

### 10 - Why do we use a build process ?
  I don't know, I have a hard time remembering what a build process is, sorry.





  NYCDA Backend Exam - Part 2

Given that we have a "customer" resource/model in our web server,

1 - How would you design the routes of your server based on REST convention? List them with VERB and /route

  GET app.get (returns input in a browser)
  POST app.post (you post data in the browser, and you can read it using req.body, then you can story it in the database using sql)
  SET app.set (updates data, also used for example to set the view engine to an extension, like pug)
  DELETE app.delete (deletes data from the database)
  USE app.use (this will get the required middlewares functioning)


2 - Which pages would require templates, and how would you name them? List them with /route and template-name.extension
  a page that creates or edits a new page for a user or a book, movie, etc.
  a page that shows the users, books, movies etc.
  public/views/new.pug


3 - What is a database constraint? Name the 3 types of database constraints you have learned.
  it's a condition that the information in the database has to obey.
  the primary key has a unique position, no other row can have that position, it's often an ID.
  the foreign key will use information from another table. for instance if you have another emailadress.
  and you can decide you own conditions, eg not null, or needs a capital letter, etc.


4 - What is a foreign key? Given that you have a Factory that has many cars and car that belongs to a factory, What would be your foreign key column?
  this example really confuses me, but a foreign key is when data references data in another table. example:

  table 1:
  id = 1; username = ivdp emailadress = ivdp@mail.com
  id = 2; username = bvda emailadress = bvda@mail.com

  table 2
  id = 1; idInTable1 = 2; username = bvda; emailadress = bvda@mail.com

5 - List all the model lifecycle hooks you have learned from sequelize and explain them briefly if necessary.

  create: creates a table.
  update: updates data in the table
  destroy: deletes data/ table

6 - What is the difference between database-level validations and application-level validations?

  I don't know!

7 - Why do we use bcrypt. Write down 3 reasons why we use it if you can.
  we use it to store passwords and other sensitive information. it's a password hashing function, it turns your password into a 60 digit hash containing all letters, capitals, numbers and the $ symbol. you store the hash in the database instead of the password, so that no-one can get access to the passwords.

8 - What is a flash message?
  it's a pop up message, for instance  for a warning, of when a password is not correctly filled in (eg. missing a number)

9 - What is the difference between minifying and obfuscating JavaScript?

  if you minify your code, it will turn into a string without spaces. if you obfuscate your code, your variables will be replaced with shorter names bu the computer: 1 symbol.

10 - What are the 3 reasons that makes Gulp a good choice as an asset build library?

  well, I have no frame of reference, but it can organize you files, minify them, uglify, obfuscate, de-obfuscate, watch, so you don't have to restart all the time, so you have a lot of options, I understood it's good for front-end organisation.
