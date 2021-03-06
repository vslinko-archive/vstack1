# vstack/lib/util

## [vstack/lib/util/invariant]

Assert function with pretty API. Used [React.js implementation].

### Usage

```js
invariant(
    post.comments.length > 0,
    'Post "%s" should have comments',
    post.title
);
```


## [vstack/lib/util/mergeInto]

Merge one object into another. Based on [React.js mergeInto].

### Differences from [React.js mergeInto]

* My implementation returns first argument after merging.

### Usage

```js
var a = {a: 1};
var b = {b: 2};
expect(mergeInto(a, b)).toBe(a);
expect(a).toEqual({a: 1, b: 2});
```


## [vstack/lib/util/update]

Simple API to change immutable objects. Used [update from React.js addons].

### Usage

```js
var a = {a: 1};
var b = {b: 2};
var c = update(a, {b: {$set: b});
expect(c).toEqual({a: 1, b: {b: 2});
```


[vstack/lib/util/invariant]: https://github.com/vslinko/vstack/blob/master/lib/util/invariant.js
[vstack/lib/util/mergeInto]: https://github.com/vslinko/vstack/blob/master/lib/util/mergeInto.js
[vstack/lib/util/update]: https://github.com/vslinko/vstack/blob/master/lib/util/update.js
[React.js implementation]: https://github.com/facebook/react/blob/master/src/vendor/core/invariant.js
[React.js mergeInto]: https://github.com/facebook/react/blob/master/src/vendor/core/mergeInto.js
[update from React.js addons]: https://github.com/facebook/react/blob/master/src/addons/update.js
