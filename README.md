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

Contributions welcome, please create issues!
