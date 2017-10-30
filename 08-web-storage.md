# Web Storage

Use [caniuse.com]() to determine which browsers support web storage. Do yours?

What kinds of applications might benefit from local storage?

Using the JavaScript console, perform the following:

1. `'localStorage' in window;`	// does this return true or false?
2. `localStorage.setItem('myName’, 'Fergal');`
3. Check that this item has been added, using the browser's developer tools. In Chrome: dev tools -> 'Application' tab -> 'Storage'.
4. `localStorage['age'] = '17';`
5. `localStorage.location = 'Northern Ireland';`
6. Retrieve the items you just set, using both the `getItem()` method, and the JavaScript object notation (square brackets or dot syntax)
7. Find the number of key-value pairs stored in localStorage, using the `.length` property.
8. Iterate over the keys and values using a for(...;...;...) loop. [You can retrieve a key at a specific index using `localStorage.key(index)`.]
9. Remove a specific item from localStorage. Check that this item has indeed been removed.
10. Remove all local storage data. Check that this has been done.
