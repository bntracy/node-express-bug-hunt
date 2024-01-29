# Node & Express Bug Hunt!

**READ ALL INSTRUCTIONS BEFORE STARTING**

There are 10 bugs in total, can you find them all? There are hints throughout (???), you should only need to make minor modifcations to 10 lines of code.

**Don't race through the files looking for the issues!** They should all have a console log or error that help you identify them. Read the console so that you know what error will cause each bug. The last one is tricky since it doesn't throw any errors. Document the error, line number and your fix in this README for each of the bugs.

## Setup
```
npm install
npm start
```

> NOTE: A couple of bugs prevent the server from starting.

## Error List

TODO: Add the error here followed by the line of code you fixed.

### Bug 0

`ReferenceError: app is not defined`

Fixed `quote.router.js` line 28: switch `app` to `router`. _This is the solution to the first bug._

### Bug 1

`TypeError: Router.use() requires a middleware function but got a Object`

Added line 28 to `quote.router.js`: `module.exports = router;`

### Bug 2

Browser returns `Cannot GET /` when navigating to `localhost:5007`.

Fixed `server.js` line 17: switch `'public'` to `'server/public'`.

### Bug 3

`GET http://localhost:5007/quotes%7D 404 (Not Found)`

Fixed `client.js` line 7: change `url: '/quotes}'` to `url: '/quotes'`, removing the bracket

### Bug 4

`GET http://localhost:5007/quotes 404 (Not Found)`

Fixed `quote.router.js` line 8: change `'/quotes'` to `'/'`

### Bug 5

`TypeError: quotesFromServer is not iterable`

Fixed `quote.router.js` line 5: change `{}` to `[]` so we're sending an array, not an object

## Extra Practice (Optional)

Complete the JS debugging exercises at:

- https://education.launchcode.org/intro-to-professional-web-dev/chapters/errors-and-debugging/exercises.html
