## MDN URLSearchParams

URLSearchParams interface defines utility methods to work with the queried string of a URL

Methods of the URLSearchParams
- .append(name, value)      params.append('foo', 4);
- .delete(name)     params.delete('foo');
- .entries()
```
- .forEach(callback)        searchParams.forEach(function(value, key) {
                                console.log(value, key);
                            });

```
- .get(name)        params.get("age")
- .getAll(name)     params.getAll('foo')
- .has(name)        params.has('bar')  
- .keys()
- .set(name, value)     params.set('baz', 3);
- .sort()
- .toString()
- .values()
## On hash change

onhashchange is an event that can be used in eventlisteners

##Location

The Location interface represents the location (URL) of the object it is linked to. Changes done on it are reflected on the object it relates to. Both the Document and Window interface have such a linked Location, accessible via Document.location and Window.location respectively.

Location has a whole list of properties for working with it
- .ancestorOrigins
- .href
- .protocol
- .host
- .hostname
- .port
- .pathname
- .search
- .hash
- .origin

Location has a whole list of methods for working with it
- .assign()
- .reload()
- .replace() -- disables navigating back to page through browser back button
- .toString()


This is a structure of a url writen in html
```
<span id="href">
    <span id="origin">
        <span id="protocol">http:</span>    
        //
        <span id="host">
            <span id="hostname">example.org</span>  
            :
            <span id="port">8888</span>
        </span>
    </span>
    
    <span id="pathname">/foo/bar</span>
    <span id="search">?q=baz</span>
    <span id="hash">#bang</span>
</span>
```

Links have a whole bunch of attributes example below
```
// Create anchor element and use href property for the purpose of this example
// A more correct alternative is to browse to the URL and use document.location or window.location
var url = document.createElement('a');
url.href = 'https://developer.mozilla.org:8080/en-US/search?q=URL#search-results-close-container';
console.log(url.href);      // https://developer.mozilla.org:8080/en-US/search?q=URL#search-results-close-container
console.log(url.protocol);  // https:
console.log(url.host);      // developer.mozilla.org:8080
console.log(url.hostname);  // developer.mozilla.org
console.log(url.port);      // 8080
console.log(url.pathname);  // /en-US/search
console.log(url.search);    // ?q=URL
console.log(url.hash);      // #search-results-close-container
console.log(url.origin);    // https://developer.mozilla.org:8080
```
