# EJS
* When creating quick on-the-fly Node applications, an easy and fast way to template our application is sometimes necessary.

**File Structure**
- Here are the files we’ll need for our application. We’ll do our templating inside of the views folder and the rest is pretty standard Node practices.

```
- views
----- partials
---------- footer.ejs
---------- head.ejs
---------- header.ejs
----- pages
---------- index.ejs
---------- about.ejs
- package.json
- server.js
```

* With all of our dependencies installed, let’s configure our application to use EJS and set up our routes for the two pages we need: the index page (full width) and the about page (sidebar). We will do all of this inside our server.js file.

`app.set('view engine', 'ejs');`

* Here we define our application and set it to show on port 8080. We also have to set EJS as the view engine for our Express application using app.set('view engine', 'ejs');. Notice how we send a view to the user by using res.render(). It is important to note that res.render() will look in a views folder for the view. So we only have to define pages/index since the full path is views/pages/index.



*Start Up our Server*
- Go ahead and start the server using:
  `node server.js`

**Create the EJS Partials**
 - Like a lot of the applications we build, there will be a lot of code that is reused. We’ll call those partials and define three files we’ll use across all of our site: head.ejs, header.ejs, and footer.ejs. Let’s make those files now.

**Add the EJS Partials to Views**
* We have our partials defined now. All we have to do is include them in our views. Let’s go into index.ejs and about.ejs and use the include syntax to add the partials.

- Syntax for including an EJS Partial
Use `<%- include('RELATIVE/PATH/TO/FILE') %>` to embed an EJS partial in another file.

- The hyphen `<%- instead of just <% to tell EJS to render raw HTML`.
The path to the partial is relative to the current file.


```
<%- include('../partials/head'); %>
</head>
<body class="container">

<header>
    <%- include('../partials/header'); %>
</header>

<main>
    <div class="jumbotron">
        <h1>This is great</h1>
        <p>Welcome to templating using EJS</p>
    </div>
</main>

<footer>
    <%- include('../partials/footer'); %>
```
**Pass Data to Views and Partials**
Let’s define some basic variables and a list to pass to our home page. Go back into your server.js file and add the following inside your app.get('/') route.


**Pass Data to a Partial in EJS**
* The EJS partial has access to all the same data as the parent view. But be careful: If you are referencing a variable in a partial, it needs to be defined in every view that uses the partial or it will throw an error.



* But you need to again be careful about assuming a variable has been defined.

If you want to reference a variable in a partial that may not always be defined, and give it a default value, you can do so like this:

`<em>Variant: <%= typeof variant != 'undefined' ? variant : 'default' %></em>`

**Conclusion**
- EJS lets us spin up quick applications when we don’t need anything too complex. By using partials and having the ability to easily pass variables to our views, we can build some great applications quickly.
