Promises
===

[![Promises](http://img.youtube.com/vi/llDikI2hTtk/0.jpg)](http://www.youtube.com/watch?v=llDikI2hTtk)

A promise represents a value that may not be available yet. The primary method for interacting with a promise is its <code>.then()</code> method.

An example promise

```javascript
var myPromise = (function() {
  var defer = Promises();

  console.log(new Date());
  
  setTimeout(function() {

    console.log(new Date());
    
    defer.fulfill('inside promise');
    
  }, 2000);
  return defer;
}());


myPromise.then(function(text) {
  alert(text);
});
```
