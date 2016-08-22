# Tips

* [Drops](https://kickdrop.me/drops)
* [Nice tips](http://arqex.com/939/learning-much-javascript-one-line-code)
* [**JS Tips**](http://www.jstips.co/)

```js
// querySelectorAll return a NodeList, an array-like list
var nodes = document.querySelectorAll('a');

// In order to iterate it, we cannot use forEach, but we can sort of duck type it
[].forEach.call(nodes, function(el, i) {
});
```

```js
JSON.stringify(json, null, 4)
```

## Netflix autocomplete search

http://www.youtube.com/watch?v=XRYN2xt11Ek

* [Learn RX](http://jhusain.github.io/learnrx/)
* [RxJava](https://github.com/Netflix/RxJava/wiki/Observable)
* [RxJS](https://github.com/Reactive-Extensions/RxJS)

```js
var searchResultSets = keyPresses
  .throttle(250)
  .map(function(key) {
    getJSON("/searchResults?q=" + input.value).retry(3)
      .takeUtil(keyPresses)
  }).concatAll();
  
searchResultSets.forEach(function(resultSet) {
  updateSearchResults(resultSet);
});
```