### Conceptual Exercise

Answer the following questions below:

- What are important differences between Python and JavaScript?
  -Python is used mainly for back-end web applications whereas JavaScript can create back-end as well as front-end applications. Python is easier to read and maintain than JavaScript. Python needs an interpreter whereas JavaScript is read by the browser. Python allows for comparisons of dictionaries and lists and JavaScript does not.

- Given a dictionary like `{"a": 1, "b": 2}`: , list two ways you
  can try to get a missing key (like "c") _without_ your programming
  crashing.
  -First you can use a get request dict.get{"c": 3}.
  -Second you could try a

  ```py
  -try: dict['student']
  -except: print("Not a key")
  ```

- What is a unit test?
- A unit test tests one area of functionality like a function or method but does not involve integration of the framework.

- What is an integration test?
- An integration test involves different functions and methods and how they interact with one another. They are written with unittest framework.

- What is the role of web application framework, like Flask?
- The role of Flask is to provide server side code on the back end like which requests to respond to and how to respond to these requests so we don't have to worry about writing the code. It has a collection of libraries and modules that developers can use to easily build web applications.

- You can pass information to Flask either as a parameter in a route URL
  (like '/foods/pretzel') or using a URL query param (like
  'foods?type=pretzel'). How might you choose which one is a better fit
  for an application?

  -A route URL would more likely be used as a subject whereas the Query Parameter has extra info as if it was entered from a form. It will ultimately depend on the application itself.

- How do you collect data from a URL placeholder parameter using Flask?

Use the variable as a parameter in the route.

```py
  @app.route('/foods/<food>)
  def grocery(food)
      x = food
```

- How do you collect data from the query string using Flask?

Using the request.args dictionary.

```py
  @app.route('/foods')
  def grocery():
      x = request.args.get('type')
```

- How do you collect data from the body of the request using Flask?

Using the request.form dictionary.

```py
  @app.route('/foods')
  def grocery():
      x = request.form.get('type')
```

- What is a cookie and what kinds of things are they commonly used for?

A cookie stores information from the server such as the domain, key and value so the user can go back to the website and have the site remember they were there before.

- What is the session object in Flask?

It is a single object that stores the user's info so they don't need multiple cookies.

- What does Flask's `jsonify()` do?

It parses json to a string so it can be easily read.
