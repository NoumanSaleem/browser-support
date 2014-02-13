browser-support
===============

Check if client browser matches rules defined with semver syntax in Node.js

###Installation
```
$ npm install browser-check
```

##Examples
###Redirect users using IE versions below 8 using Express.js

```
var browserCheck = require('browser-check');
app.use(function (req, res, next) {
	var unsupported = browserCheck(req.headers['user-agent'], { "IE": "<8" });
	if (unsupported) return res.redirect('http://google.com');
	next();
});
```
