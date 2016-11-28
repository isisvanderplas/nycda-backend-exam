## NYCDA Backend Exam
=====================
Explain the questions well!!

### 1- Why do we should include script tags at the very end of an html file, before closing </body>?
  it will make the page load faster, at least easthetically, because now the computer can read all the code first and show it, instead of stopping to read the scripts first. the website will fully function once all the script tags are read, but it looks finished to the client side.

### 2 - What is a middleware?
    a middleware is a small software that you download and require, because it doesn't come with the operating system. It runs between the client and the serverside, it's been described as "glue".

### 3 - Why do we use express.static() middleware?
  it enables static files to be used.

### 4 - What is favicon.ico ?
  the little picture you see in the tab on the left of the site name

### 5 - Why do we use a bodyParser middleware ?
  when yo use POST, you need the body-parsing middleware to make the req.body readable to us, puny humans.

### 6 - What is the difference in terms of parsing a data received from a web form with POST or an AJAX POST request?
  (I'm not sure if I understand the question, but here goes)
  AJAX will make a "live" post. it will be immediatley visible to the client side, they don't have to renew the page to see the post. eg. a chat.

### 7 - Why do we use methodOverride middleware ?
  sometimes the client side doesn't support our code, maybe because of an old browser. because of this middleware, the site can still be used.

### 8 - What are the differences between sessions and cookies ?
  session is temporary, it lasts one session, cookies will last until the client deletes them

### 9 - Why do we use a session middleware ?
  to keep the client logged in, even if they renew the page

### 10 - Why do we use a build process ?
  I don't know, I have a hard time remembering what a build process is, sorry.
