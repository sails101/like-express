# like-express

How do I use Sails programmatically, or with my own custom file structure?

This code is the verbatim output of the [sails-generate-new-but-like-express]() generator.  It is an example is designed to look exactly like a boilerplate Express app to demonstrate that you can set up your Sails project however you like, and load your business logic in many different ways

Note that you cannot run this project using `sails lift`.  You need to do run `npm start` (which calls `node app.js`).  See `app.js` to see how it works.


**tldr:**

From `app.js`:

```js
// Configure and lift app
var app = new Sails();
app.lift({
  port: 1337,
  views: { engine: 'jade', layout: false },
  hooks: { grunt: false },
  globals: false,
  routes: {
    'get /': function (req, res){ ... },
    'get /users': function (req, res) { ... }
  }
});
```


### License

MIT
