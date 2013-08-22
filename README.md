Promises
===

[![Promises](http://img.youtube.com/vi/llDikI2hTtk/0.jpg)](http://www.youtube.com/watch?v=llDikI2hTtk)

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
