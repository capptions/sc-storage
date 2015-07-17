sc-storage
============

Polymer 1.0 element for easy localStorage access

`<sc-storage>` is an element that exposes localStorage api's in a friendly way, especially for storing JSON

## Getting started

### Install with bower

First you need bower, [see their site](http://bower.io/) for details 

```
bower install --save sc-storage
```

### API

| Method Name | Functionality |
|----------------|-------------|
| get | Get an object using parameter `key` |
| set | Set an object using parameter `key` and value `object` |
| push | Push to an array saved under parameter `key` with value `object`, alternatively passing `unshift` as true |
| shift | Shift the first item from an array saved under paramter `key` and return it |

### How to use

```html
  <sc-storage></sc-storage>
```

### Example usage

```
  var ls = document.getElementsByTagName('sc-storage')[0];

  // Set the object
  ls.set(0, {
    name: 'superman',
    address: 'krypton'
  });

  // Get the object
  ls.get(0);

  // Push the value at a specifty position
  ls.push(1, { age: 30 }, 'unshift');

  // Remove the element from index 1
  ls.shift(1)

  // Clear the local storage
  ls.clear();


```

Contributions welcome, please create issues!
