## `ResolutionPolicy` Class



Module: [_decorator](../modules/_decorator.md)
Parent Module: [cc](../modules/cc.md)


<p>cc.ResolutionPolicy class is the root strategy class of scale strategy,
its main task is to maintain the compatibility with Cocos2d-x</p>


### Index

##### Properties

  - [`EXACT_FIT`](#exactfit) `Number` The entire application is visible in the specified area without trying to preserve the original aspect ratio....
  - [`NO_BORDER`](#noborder) `Number` The entire application fills the specified area, without distortion but possibly with some cropping,...
  - [`SHOW_ALL`](#showall) `Number` aspect ratio of the application.
  - [`FIXED_HEIGHT`](#fixedheight) `Number` The application takes the height of the design resolution size and modifies the width of the internal...
  - [`FIXED_WIDTH`](#fixedwidth) `Number` The application takes the width of the design resolution size and modifies the height of the internal...
  - [`UNKNOWN`](#unknown) `Number` Unknow policy



##### Methods

  - [`constructor`](#constructor) 
  - [`preApply`](#preapply) Manipulation before applying the resolution policy
  - [`apply`](#apply) Function to apply this resolution policy
  - [`postApply`](#postapply) Manipulation after appyling the strategy
  - [`setContainerStrategy`](#setcontainerstrategy) Setup the container's scale strategy
  - [`setContentStrategy`](#setcontentstrategy) Setup the content's scale strategy



### Details


#### Properties


##### EXACT_FIT

> The entire application is visible in the specified area without trying to preserve the original aspect ratio.<br/>
Distortion can occur, and the application may appear stretched or compressed.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1469](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1469) |



##### NO_BORDER

> The entire application fills the specified area, without distortion but possibly with some cropping,<br/>
while maintaining the original aspect ratio of the application.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1478](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1478) |



##### SHOW_ALL

> The entire application is visible in the specified area without distortion while maintaining the original<br/>
aspect ratio of the application. Borders can appear on two sides of the application.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1487](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1487) |



##### FIXED_HEIGHT

> The application takes the height of the design resolution size and modifies the width of the internal<br/>
canvas so that it fits the aspect ratio of the device<br/>
no distortion will occur however you must make sure your application works on different<br/>
aspect ratios

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1496](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1496) |



##### FIXED_WIDTH

> The application takes the width of the design resolution size and modifies the height of the internal<br/>
canvas so that it fits the aspect ratio of the device<br/>
no distortion will occur however you must make sure your application works on different<br/>
aspect ratios

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1507](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1507) |



##### UNKNOWN

> Unknow policy

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCView.js:1518](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1518) |






<!-- Method Block -->
#### Methods


##### constructor



| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCView.js:1391](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1391) |

###### Parameters
- `containerStg` <a href="../classes/ContainerStrategy.html" class="crosslink">ContainerStrategy</a> The container strategy
- `contentStg` <a href="../classes/ContentStrategy.html" class="crosslink">ContentStrategy</a> The content strategy


##### preApply

Manipulation before applying the resolution policy

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCView.js:1410](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1410) |

###### Parameters
- `view` <a href="../classes/View.html" class="crosslink">View</a> The target view


##### apply

Function to apply this resolution policy
The return value is {scale: [scaleX, scaleY], viewport: {cc.Rect}},
The target view can then apply these value to itself, it's preferred not to modify directly its private variables

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
| Defined in | [cocos2d/core/platform/CCView.js:1420](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1420) |

###### Parameters
- `view` <a href="../classes/View.html" class="crosslink">View</a> The target view
- `designedResolution` <a href="../classes/Size.html" class="crosslink">Size</a> The user defined design resolution


##### postApply

Manipulation after appyling the strategy

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCView.js:1434](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1434) |

###### Parameters
- `view` <a href="../classes/View.html" class="crosslink">View</a> The target view


##### setContainerStrategy

Setup the container's scale strategy

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCView.js:1444](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1444) |

###### Parameters
- `containerStg` <a href="../classes/ContainerStrategy.html" class="crosslink">ContainerStrategy</a> 


##### setContentStrategy

Setup the content's scale strategy

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCView.js:1454](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCView.js#L1454) |

###### Parameters
- `contentStg` <a href="../classes/ContentStrategy.html" class="crosslink">ContentStrategy</a> 



