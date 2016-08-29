# Backbone.js Tutorial - TODO app

Following tutorial from http://adrianmejia.com/blog/2012/09/13/backbone-js-for-absolute-beginners-getting-started-part-2/.

## Backbone Views
 * similar to Controller in MVC framework
   * glue together user events (clicks, pressed keys, etc.)
   * render HTML views and templates
   * interact with models which contains the data of the application
 * every view has an element associated in HTML content that will be rendered
 * first calls function `initialize` when view is instantiated

## Templates in Backbone (using `underscore.js`)
 `_.js` template syntax:
  * `_.template (templateString, [data], [settings])`
  	  * `<%= %>` does not allow for HTML escape
  	  * `<%- %>`allows for HTML escape
  	  * `<% %>` to run any JS code

## Backbone Models
 * contains interactive data & logic
    * data validation, getters & setters, default values, data initialization, conversions
 * capitalize class names, don't capitalize instance variables and objects
 * properties are dynamic

Example: model `Todo` will store string of text and whether task has been completed or not.
```
var app = {}; // create namespace for our app
app.Todo = Backbone.Model.extend({
  defaults: {
    title: '',
    completed: false
  }
});
```

In console:
```
var todo = new app.Todo({title: 'Learn Backbone.js', completed: false}); // create object with the attributes specified.
todo.get('title'); // "Learn Backbone.js"
todo.get('completed'); // false
todo.get('created_at'); // undefined
todo.set('created_at', Date());
todo.get('created_at'); // "Wed Sep 12 2012 12:51:17 GMT-0400 (EDT)"
```

