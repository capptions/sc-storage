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
  <sc-storage id="storage"></sc-storage>
```

### Example usage

```
var shout = function (profile) {
  window.alert(profile.name.concat(' lives at ', profile.address!'));
};

// Store something
this.$.storage.set('profile', {
  name: 'superman',
  address: 'krypton'
});

// Retrieve something
var superman = this.$.storage.get('profile');
shout(superman);

// Push to an array
this.$.storage.push('profiles', {
  name: 'superman',
  address: 'krypton'
});

this.$.storage.push('profiles', {
  name: 'batman',
  address: 'gotham'
}, 'unshift');

// Retrieve and pop the first one from the array
var batman = this.$.storage.shift('profiles');
shout(batman);

// Clear the storage
this.$.storage.clear();
```

Contributions welcome, please create issues!
