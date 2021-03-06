
## `js` Module






This module provides some JavaScript utilities.
All members can be accessed with "cc.js".


### Classes

  - [array](../classes/array.md)
  - [Pool](../classes/Pool.md)



### Index



##### Methods

  - [`isNumber`](#isnumber) If a number is created by using 'new Number(10086)', the typeof it will be "object"...
  - [`isString`](#isstring) Check the obj whether is string or not.
  - [`addon`](#addon) This method is deprecated, use cc.js.mixin please.<br>...
  - [`mixin`](#mixin) copy all properties from arguments[1...n] to obj
  - [`extend`](#extend) Derive the class from the supplied base class.
  - [`getSuper`](#getsuper) Get super class
  - [`clear`](#clear) Removes all enumerable properties from object
  - [`getPropertyDescriptor`](#getpropertydescriptor) Get property descriptor in object and all its ancestors
  - [`value`](#value) Define value, just help to call Object.defineProperty.<br>...
  - [`getset`](#getset) Define get set accessor, just help to call Object.defineProperty(...)
  - [`get`](#get) Define get accessor, just help to call Object.defineProperty(...)
  - [`set`](#set) Define set accessor, just help to call Object.defineProperty(...)
  - [`getClassName`](#getclassname) Get class name of the object, if object is just a {} (and which class named 'Object'), it will return "".
  - [`_setClassId`](#setclassid) Register the class by specified id, if its classname is not defined, the class name will also be set.
  - [`setClassName`](#setclassname) Register the class by specified name manually
  - [`unregisterClass`](#unregisterclass) Unregister a class from fireball.
  - [`_getClassById`](#getclassbyid) Get the registered class by id
  - [`getClassByName`](#getclassbyname) Get the registered class by name
  - [`_getClassId`](#getclassid) Get class id of the object
  - [`obsolete`](#obsolete) Defines a polyfill field for obsoleted codes.
  - [`obsoletes`](#obsoletes) Defines all polyfill fields for obsoleted codes corresponding to the enumerable properties of props.
  - [`formatStr`](#formatstr) A string tool to construct a string with format string.
  - [`createMap`](#createmap) A simple wrapper of `Object.create(null)` which ensures the return object have no prototype (and thus no inherited members).



### Details




<!-- Method Block -->
#### Methods


##### isNumber

Check the obj whether is number or not
If a number is created by using 'new Number(10086)', the typeof it will be "object"...
Then you can use this function if you care about this case.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
| Defined in | [cocos2d/core/platform/js.js:58](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L58) |

###### Parameters
- `obj` Any 


##### isString

Check the obj whether is string or not.
If a string is created by using 'new String("blabla")', the typeof it will be "object"...
Then you can use this function if you care about this case.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
| Defined in | [cocos2d/core/platform/js.js:70](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L70) |

###### Parameters
- `obj` Any 


##### addon

This method is deprecated, use cc.js.mixin please.<br>
Copy all properties not defined in obj from arguments[1...n]

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
| Defined in | [cocos2d/core/platform/js.js:82](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L82) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> object to extend its properties
- `sourceObj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> source object to copy properties from


##### mixin

copy all properties from arguments[1...n] to obj

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
| Defined in | [cocos2d/core/platform/js.js:111](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L111) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `sourceObj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 


##### extend

Derive the class from the supplied base class.
Both classes are just native javascript constructors, not created by cc.Class, so
usually you will want to inherit using <a href="../modules/cc.html#method_Class" class="crosslink">cc.Class</a> instead.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
| Defined in | [cocos2d/core/platform/js.js:136](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L136) |

###### Parameters
- `cls` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
- `base` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> the baseclass to inherit


##### getSuper

Get super class

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
| Defined in | [cocos2d/core/platform/js.js:170](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L170) |

###### Parameters
- `ctor` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> the constructor of subclass


##### clear

Removes all enumerable properties from object

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:189](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L189) |

###### Parameters
- `obj` Any 


##### getPropertyDescriptor

Get property descriptor in object and all its ancestors

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
| Defined in | [cocos2d/core/platform/js.js:201](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L201) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `name` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 


##### value

Define value, just help to call Object.defineProperty.<br>
The configurable will be true.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:219](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L219) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `prop` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `value` Any 
- `writable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
- `enumerable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### getset

Define get set accessor, just help to call Object.defineProperty(...)

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:243](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L243) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `prop` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `getter` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
- `setter` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
- `enumerable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### get

Define get accessor, just help to call Object.defineProperty(...)

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:271](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L271) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `prop` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `getter` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
- `enumerable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
- `configurable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### set

Define set accessor, just help to call Object.defineProperty(...)

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:294](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L294) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `prop` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `setter` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
- `enumerable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
- `configurable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### getClassName

Get class name of the object, if object is just a {} (and which class named 'Object'), it will return "".
(modified from <a href="http://stackoverflow.com/questions/1249531/how-to-get-a-javascript-objects-class">the code from this stackoverflow post</a>)

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
| Defined in | [cocos2d/core/platform/js.js:311](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L311) |

###### Parameters
- `objOrCtor` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> instance or constructor


##### _setClassId

Register the class by specified id, if its classname is not defined, the class name will also be set.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:389](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L389) |

###### Parameters
- `classId` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `constructor` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 


##### setClassName

Register the class by specified name manually

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:400](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L400) |

###### Parameters
- `className` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
- `constructor` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 


##### unregisterClass

Unregister a class from fireball.

If you dont need a registered class anymore, you should unregister the class so that Fireball will not keep its reference anymore.
Please note that its still your responsibility to free other references to the class.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:417](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L417) |

###### Parameters
- `constructor` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> the class you will want to unregister, any number of classes can be added


##### _getClassById

Get the registered class by id

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
| Defined in | [cocos2d/core/platform/js.js:440](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L440) |

###### Parameters
- `classId` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 


##### getClassByName

Get the registered class by name

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> 
| Defined in | [cocos2d/core/platform/js.js:451](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L451) |

###### Parameters
- `classname` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 


##### _getClassId

Get class id of the object

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
| Defined in | [cocos2d/core/platform/js.js:461](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L461) |

###### Parameters
- `obj` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> instance or constructor
- `allowTempId` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> can return temp id in editor


##### obsolete

Defines a polyfill field for obsoleted codes.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:528](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L528) |

###### Parameters
- `obj` Any YourObject or YourClass.prototype
- `obsoleted` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> "OldParam" or "YourClass.OldParam"
- `newExpr` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> "NewParam" or "YourClass.NewParam"
- `writable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### obsoletes

Defines all polyfill fields for obsoleted codes corresponding to the enumerable properties of props.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/js.js:562](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L562) |

###### Parameters
- `obj` Any YourObject or YourClass.prototype
- `objName` Any "YourObject" or "YourClass"
- `props` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
- `writable` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### formatStr

A string tool to construct a string with format string.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 
| Defined in | [cocos2d/core/platform/js.js:580](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L580) |

###### Parameters
- `msg` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> &#124; Any A JavaScript string containing zero or more substitution strings (%s).
- `subst` Any JavaScript objects with which to replace substitution strings within msg. This gives you additional control over the format of the output.

##### Examples

```js
cc.js.formatStr("a: %s, b: %s", a, b);
cc.js.formatStr(a, b, c);
```

##### createMap

A simple wrapper of `Object.create(null)` which ensures the return object have no prototype (and thus no inherited members). So we can skip `hasOwnProperty` calls on property lookups. It is a worthwhile optimization than the `{}` literal when `hasOwnProperty` calls are necessary.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> 
| Defined in | [cocos2d/core/platform/js.js:629](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/js.js#L629) |

###### Parameters
- `forceDictMode` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> Apply the delete operator to newly created map object. This causes V8 to put the object in "dictionary mode" and disables creation of hidden classes which are very expensive for objects that are constantly changing shape.



