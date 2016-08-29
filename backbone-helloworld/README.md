# Backbone.js Tutorial - absolute beginner

Following tutorial from http://adrianmejia.com/blog/2012/09/11/backbone-dot-js-for-absolute-beginners-getting-started/.

## Backbone Views
 * similar to Controller in MVC framework
 * every view has an element associated in HTML content that will be rendered
 * first calls function `initialize` when view is instantiated

 ## Templates in Backbone (using `underscore.js`)
 `_.js` template syntax:
  * `_.template (templateString, [data], [settings])`
  	  * `<%= %>` does not allow for HTML escape
  	  * `<%- %>`allows for HTML escape
  	  * `<% %>` to run any JS code