## `Pipeline.Loader` Class



Module: [cc](../modules/cc.md)
Parent Module: [cc](../modules/cc.md)


The loader pipe, it can load several types of files:
1. Images
2. JSON
3. Plist
4. Audio
5. Font
6. Cocos Creator scene
It will not interfere with items of unknown type.
You can pass custom supported types in the constructor.


### Index



##### Methods

  - [`constructor`](#constructor) Constructor of Loader, you can pass custom supported types.
  - [`addHandlers`](#addhandlers) Add custom supported types handler or modify existing type handler.



### Details




<!-- Method Block -->
#### Methods


##### constructor

Constructor of Loader, you can pass custom supported types.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/load-pipeline/loader.js:152](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/load-pipeline/loader.js#L152) |

###### Parameters
- `extMap` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> Custom supported types with corresponded handler

##### Examples

```js
var loader = new Loader({
   // This will match all url with `.scene` extension or all url with `scene` type
   'scene' : function (url, callback) {}
});
```

##### addHandlers

Add custom supported types handler or modify existing type handler.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/load-pipeline/loader.js:172](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/load-pipeline/loader.js#L172) |

###### Parameters
- `extMap` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> Custom supported types with corresponded handler



