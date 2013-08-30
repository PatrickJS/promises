Promises
===

[![Promises](http://img.youtube.com/vi/llDikI2hTtk/0.jpg)](http://www.youtube.com/watch?v=llDikI2hTtk)

A promise represents a value that may not be available yet. The primary method for interacting with a promise is its <code>.then()</code> method.


###Examples
```javascript
var deferred = Promises();
deferred.then(function(result) {
  alert(result);
});

deferred.fulfill('Here is my deferred text');
```
```javascript
var myPromise = (function() {
  var defer = Promises();
  
  var randomInterval = ~~(Math.random()*5000);
  console.log('randomInterval time set to ' + randomInterval + ' at ' + new Date());
  
  setTimeout(function() {

    console.log(new Date());
    
    defer.fulfill('resolved my promise');
    
  }, randomInterval);
  
  return defer;
}());


myPromise.then(function(text) {
  alert(text);
});
```
