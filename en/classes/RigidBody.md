## `RigidBody` Class

Extends [`Component`](Component.md)


Module: [cc](../modules/cc.md)
Parent Module: [cc](../modules/cc.md)





### Index

##### Properties

  - [`enabledContactListener`](#enabledcontactlistener) `Boolean` Should enabled contact listener?...
  - [`bullet`](#bullet) `Boolean` - All bodies are prevented from tunneling through kinematic and static bodies.
  - [`type`](#type) `RigidBodyType` Rigidbody type : Static, Kinematic, Dynamic or Animated.
  - [`allowSleep`](#allowsleep) `Boolean` Set this flag to false if this body should never fall asleep.
  - [`gravityScale`](#gravityscale) `Number` Scale the gravity applied to this body.
  - [`linearDamping`](#lineardamping) `Number` Linear damping is use to reduce the linear velocity.
  - [`angularDamping`](#angulardamping) `Number` Angular damping is use to reduce the angular velocity.
  - [`linearVelocity`](#linearvelocity) `Vec2` The linear velocity of the body's origin in world co-ordinates.
  - [`angularVelocity`](#angularvelocity) `Number` The angular velocity of the body.
  - [`fixedRotation`](#fixedrotation) `Boolean` Should this body be prevented from rotating?
  - [`awake`](#awake) `Boolean` Is this body initially awake or sleeping?
  - [`active`](#active) `Boolean` Set the active state of the body.
  - [`__eventTargets`](#eventtargets) `Array` Register all related EventTargets,...
  - [`node`](#node) `Node` The node this component is attached to.
  - [`uuid`](#uuid) `String` The uuid for editor.
  - [`_enabled`](#enabled) `Boolean` 
  - [`enabled`](#enabled) `Boolean` indicates whether this component is enabled or not.
  - [`enabledInHierarchy`](#enabledinhierarchy) `Boolean` indicates whether this component is enabled and its node is also active in the hierarchy.
  - [`_isOnLoadCalled`](#isonloadcalled) `Number` Returns a value which used to indicate the onLoad get called or not.
  - [`_name`](#name) `String` 
  - [`_objFlags`](#objflags) `Number` 
  - [`name`](#name) `String` The name of the object.
  - [`isValid`](#isvalid) `Boolean` Indicates whether the object is not yet destroyed.



##### Methods

  - [`onBeginContact`](#onbegincontact) Collision callback.
  - [`onEndContact`](#onendcontact) Collision callback.
  - [`onPreSolve`](#onpresolve) Collision callback.
  - [`onPostSolve`](#onpostsolve) Collision callback.
  - [`getLocalPoint`](#getlocalpoint) Gets a local point relative to the body's origin given a world point.
  - [`getWorldPoint`](#getworldpoint) Get the world coordinates of a point given the local coordinates.
  - [`getWorldVector`](#getworldvector) Get the world coordinates of a vector given the local coordinates.
  - [`getLocalVector`](#getlocalvector) Gets a local vector relative to the body's origin given a world vector.
  - [`getWorldPosition`](#getworldposition) Get the world body origin position.
  - [`getWorldRotation`](#getworldrotation) Get the world body rotation angle.
  - [`getLocalCenter`](#getlocalcenter) Get the local position of the center of mass.
  - [`getWorldCenter`](#getworldcenter) Get the world position of the center of mass.
  - [`getLinearVelocityFromWorldPoint`](#getlinearvelocityfromworldpoint) Get the world linear velocity of a world point attached to this body.
  - [`getMass`](#getmass) Get total mass of the body.
  - [`getInertia`](#getinertia) Get the rotational inertia of the body about the local origin.
  - [`getJointList`](#getjointlist) Get all the joints connect to the rigidbody.
  - [`applyForce`](#applyforce) Apply a force at a world point.
  - [`applyForceToCenter`](#applyforcetocenter) Apply a force to the center of mass.
  - [`applyTorque`](#applytorque) Apply a torque.
  - [`applyLinearImpulse`](#applylinearimpulse) Apply a impulse at a world point, This immediately modifies the velocity.
  - [`applyAngularImpulse`](#applyangularimpulse) Apply an angular impulse.
  - [`syncPosition`](#syncposition) Synchronize node's world position to box2d rigidbody's position.
  - [`syncRotation`](#syncrotation) Synchronize node's world angle to box2d rigidbody's angle.
  - [`update`](#update) Update is called every frame, if the Component is enabled.
  - [`lateUpdate`](#lateupdate) LateUpdate is called every frame, if the Component is enabled.
  - [`__preload`](#preload) `__preload` is called before every onLoad.
  - [`onLoad`](#onload) When attaching to an active node or its node first activated.
  - [`start`](#start) Called before all scripts' update if the Component is enabled the first time.
  - [`onEnable`](#onenable) Called when this component becomes enabled and its node is active.
  - [`onDisable`](#ondisable) Called when this component becomes disabled or its node becomes inactive.
  - [`onDestroy`](#ondestroy) Called when this component will be destroyed.
  - [`onFocusInEditor`](#onfocusineditor) 
  - [`onLostFocusInEditor`](#onlostfocusineditor) 
  - [`resetInEditor`](#resetineditor) Called to initialize the component or node’s properties when adding the component the first time or when the Reset command is used.
  - [`addComponent`](#addcomponent) Adds a component class to the node.
  - [`getComponent`](#getcomponent) Returns the component of supplied type if the node has one attached, null if it doesn't....
  - [`getComponents`](#getcomponents) Returns all components of supplied Type in the node.
  - [`getComponentInChildren`](#getcomponentinchildren) Returns the component of supplied type in any of its children using depth first search.
  - [`getComponentsInChildren`](#getcomponentsinchildren) Returns the components of supplied type in self or any of its children using depth first search.
  - [`_getLocalBounds`](#getlocalbounds) If the component's bounding box is different from the node's, you can implement this method to supply
  - [`onRestore`](#onrestore) for undo/redo operation.
  - [`schedule`](#schedule) Schedules a custom selector....
  - [`scheduleOnce`](#scheduleonce) Schedules a callback function that runs only once, with a delay of 0 or larger.
  - [`unschedule`](#unschedule) Unschedules a custom callback function.
  - [`unscheduleAllCallbacks`](#unscheduleallcallbacks) unschedule all scheduled callback functions: custom callback functions, and the 'update' callback function....
  - [`destroy`](#destroy) Actual object destruction will delayed until before rendering.
  - [`_destruct`](#destruct) Clear all references in the instance.
  - [`_onPreDestroy`](#onpredestroy) Called before the object being destroyed.
  - [`_serialize`](#serialize) The customized serialization for this object.
  - [`_deserialize`](#deserialize) Init this object from the custom serialized data.



### Details


#### Properties


##### enabledContactListener

> Should enabled contact listener?
When a collision is trigger, the collision callback will only be called when enabled contact listener.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:76](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L76) |



##### bullet

> Is this a fast moving body that should be prevented from tunneling through
other moving bodies?
Note :
- All bodies are prevented from tunneling through kinematic and static bodies. This setting is only considered on dynamic bodies.
- You should use this flag sparingly since it increases processing time.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:150](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L150) |



##### type

> Rigidbody type : Static, Kinematic, Dynamic or Animated.

| meta | description |
|------|-------------|
| Type | <a href="../enums/RigidBodyType.html" class="crosslink">RigidBodyType</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:170](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L170) |



##### allowSleep

> Set this flag to false if this body should never fall asleep.
Note that this increases CPU usage.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:198](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L198) |



##### gravityScale

> Scale the gravity applied to this body.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:225](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L225) |



##### linearDamping

> Linear damping is use to reduce the linear velocity.
The damping parameter can be larger than 1, but the damping effect becomes sensitive to the
time step when the damping parameter is large.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:246](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L246) |



##### angularDamping

> Angular damping is use to reduce the angular velocity. The damping parameter
can be larger than 1 but the damping effect becomes sensitive to the
time step when the damping parameter is large.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:269](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L269) |



##### linearVelocity

> The linear velocity of the body's origin in world co-ordinates.

| meta | description |
|------|-------------|
| Type | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:292](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L292) |



##### angularVelocity

> The angular velocity of the body.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:323](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L323) |



##### fixedRotation

> Should this body be prevented from rotating?

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:347](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L347) |



##### awake

> Is this body initially awake or sleeping?

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:368](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L368) |



##### active

> Set the active state of the body. An inactive body is not
simulated and cannot be collided with or woken up.
If body is active, all fixtures will be added to the
broad-phase.
If body is inactive, all fixtures will be removed from
the broad-phase and all contacts will be destroyed.
Fixtures on an inactive body are implicitly inactive and will
not participate in collisions, ray-casts, or queries.
Joints connected to an inactive body are implicitly inactive.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/physics/CCRigidBody.js:388](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L388) |



##### __eventTargets

> Register all related EventTargets,
all event callbacks will be removed in _onPreDestroy

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array" class="crosslink external" target="_blank">Array</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:62](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L62) |



##### node

> The node this component is attached to. A component is always attached to a node.

| meta | description |
|------|-------------|
| Type | <a href="../classes/Node.html" class="crosslink">Node</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:76](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L76) |

##### Examples

```js
cc.log(comp.node);
```


##### uuid

> The uuid for editor.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:112](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L112) |

##### Examples

```js
cc.log(comp.uuid);
```


##### _enabled

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:160](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L160) |



##### enabled

> indicates whether this component is enabled or not.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:167](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L167) |

##### Examples

```js
comp.enabled = true;
cc.log(comp.enabled);
```


##### enabledInHierarchy

> indicates whether this component is enabled and its node is also active in the hierarchy.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:198](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L198) |

##### Examples

```js
cc.log(comp.enabledInHierarchy);
```


##### _isOnLoadCalled

> Returns a value which used to indicate the onLoad get called or not.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/components/CCComponent.js:214](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L214) |

##### Examples

```js
cc.log(this._isOnLoadCalled > 0);
```


##### _name

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:76](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L76) |



##### _objFlags

> 

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:83](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L83) |



##### name

> The name of the object.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:243](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L243) |

##### Examples

```js
obj.name = "New Obj";
```


##### isValid

> Indicates whether the object is not yet destroyed. (It will not be available after being destroyed)<br>
When an object's `destroy` is called, it is actually destroyed after the end of this frame.
So `isValid` will return false from the next frame, while `isValid` in the current frame will still be true.
If you want to determine whether the current frame has called `destroy`, use `cc.isValid(obj, true)`,
but this is often caused by a particular logical requirements, which is not normally required.

| meta | description |
|------|-------------|
| Type | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> |
| Defined in | [cocos2d/core/platform/CCObject.js:261](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L261) |

##### Examples

```js
var node = new cc.Node();
cc.log(node.isValid);    // true
node.destroy();
cc.log(node.isValid);    // true, still valid in this frame
// after a frame...
cc.log(node.isValid);    // false, destroyed in the end of last frame
```





<!-- Method Block -->
#### Methods


##### onBeginContact

Collision callback.
Called when two collider begin to touch.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:91](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L91) |

###### Parameters
- `contact` <a href="../classes/PhysicsContact.html" class="crosslink">PhysicsContact</a> contact information
- `selfCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to this rigidbody
- `otherCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to another rigidbody


##### onEndContact

Collision callback.
Called when two collider cease to touch.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:103](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L103) |

###### Parameters
- `contact` <a href="../classes/PhysicsContact.html" class="crosslink">PhysicsContact</a> contact information
- `selfCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to this rigidbody
- `otherCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to another rigidbody


##### onPreSolve

Collision callback.
This is called when a contact is updated.
This allows you to inspect a contact before it goes to the solver(e.g. disable contact).
Note: this is called only for awake bodies.
Note: this is called even when the number of contact points is zero.
Note: this is not called for sensors.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:115](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L115) |

###### Parameters
- `contact` <a href="../classes/PhysicsContact.html" class="crosslink">PhysicsContact</a> contact information
- `selfCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to this rigidbody
- `otherCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to another rigidbody


##### onPostSolve

Collision callback.
This is called after a contact is updated.
You can get the impulses from the contact in this callback.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:135](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L135) |

###### Parameters
- `contact` <a href="../classes/PhysicsContact.html" class="crosslink">PhysicsContact</a> contact information
- `selfCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to this rigidbody
- `otherCollider` <a href="../classes/PhysicsCollider.html" class="crosslink">PhysicsCollider</a> the collider belong to another rigidbody


##### getLocalPoint

Gets a local point relative to the body's origin given a world point.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:421](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L421) |

###### Parameters
- `worldPoint` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> a point in world coordinates.
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving point


##### getWorldPoint

Get the world coordinates of a point given the local coordinates.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:442](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L442) |

###### Parameters
- `localPoint` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> a point in local coordinates.
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving point


##### getWorldVector

Get the world coordinates of a vector given the local coordinates.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:463](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L463) |

###### Parameters
- `localVector` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> a vector in world coordinates.
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving vector


##### getLocalVector

Gets a local vector relative to the body's origin given a world vector.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:484](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L484) |

###### Parameters
- `worldVector` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> a vector in world coordinates.
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving vector


##### getWorldPosition

Get the world body origin position.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:505](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L505) |

###### Parameters
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving point


##### getWorldRotation

Get the world body rotation angle.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:524](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L524) |



##### getLocalCenter

Get the local position of the center of mass.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:539](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L539) |



##### getWorldCenter

Get the world position of the center of mass.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:557](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L557) |



##### getLinearVelocityFromWorldPoint

Get the world linear velocity of a world point attached to this body.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Vec2.html" class="crosslink">Vec2</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:575](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L575) |

###### Parameters
- `worldPoint` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> a point in world coordinates.
- `out` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> optional, the receiving point


##### getMass

Get total mass of the body.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:596](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L596) |



##### getInertia

Get the rotational inertia of the body about the local origin.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:608](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L608) |



##### getJointList

Get all the joints connect to the rigidbody.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Joint.html" class="crosslink">[Joint]</a> 
| Defined in | [cocos2d/core/physics/CCRigidBody.js:620](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L620) |



##### applyForce

Apply a force at a world point. If the force is not
applied at the center of mass, it will generate a torque and
affect the angular velocity.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:664](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L664) |

###### Parameters
- `force` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> the world force vector.
- `point` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> the world position.
- `wake` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> also wake up the body.


##### applyForceToCenter

Apply a force to the center of mass.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:684](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L684) |

###### Parameters
- `force` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> the world force vector.
- `wake` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> also wake up the body.


##### applyTorque

Apply a torque. This affects the angular velocity.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:700](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L700) |

###### Parameters
- `torque` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> about the z-axis (out of the screen), usually in N-m.
- `wake` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> also wake up the body


##### applyLinearImpulse

Apply a impulse at a world point, This immediately modifies the velocity.
If the impulse is not applied at the center of mass, it will generate a torque and
affect the angular velocity.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:715](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L715) |

###### Parameters
- `impulse` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> the world impulse vector, usually in N-seconds or kg-m/s.
- `point` <a href="../classes/Vec2.html" class="crosslink">Vec2</a> the world position
- `wake` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> alse wake up the body


##### applyAngularImpulse

Apply an angular impulse.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:736](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L736) |

###### Parameters
- `impulse` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> the angular impulse in units of kg*m*m/s
- `wake` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> also wake up the body


##### syncPosition

Synchronize node's world position to box2d rigidbody's position.
If enableAnimated is true and rigidbody's type is Animated type,
will set linear velocity instead of directly set rigidbody's position.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:751](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L751) |

###### Parameters
- `enableAnimated` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### syncRotation

Synchronize node's world angle to box2d rigidbody's angle.
If enableAnimated is true and rigidbody's type is Animated type,
will set angular velocity instead of directly set rigidbody's angle.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/physics/CCRigidBody.js:796](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/physics/CCRigidBody.js#L796) |

###### Parameters
- `enableAnimated` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### update

Update is called every frame, if the Component is enabled.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:235](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L235) |

###### Parameters
- `dt` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> the delta time in seconds it took to complete the last frame


##### lateUpdate

LateUpdate is called every frame, if the Component is enabled.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:244](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L244) |



##### __preload

`__preload` is called before every onLoad.
It is used to initialize the builtin components internally,
to avoid checking whether onLoad is called before every public method calls.
This method should be removed if script priority is supported.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:252](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L252) |



##### onLoad

When attaching to an active node or its node first activated.
onLoad is always called before any start functions, this allows you to order initialization of scripts.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:263](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L263) |



##### start

Called before all scripts' update if the Component is enabled the first time.
Usually used to initialize some logic which need to be called after all components' `onload` methods called.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:274](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L274) |



##### onEnable

Called when this component becomes enabled and its node is active.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:285](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L285) |



##### onDisable

Called when this component becomes disabled or its node becomes inactive.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:293](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L293) |



##### onDestroy

Called when this component will be destroyed.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:301](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L301) |



##### onFocusInEditor



| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:309](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L309) |



##### onLostFocusInEditor



| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:314](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L314) |



##### resetInEditor

Called to initialize the component or node’s properties when adding the component the first time or when the Reset command is used. This function is only called in editor.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:319](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L319) |



##### addComponent

Adds a component class to the node. You can also add component to node by passing in the name of the script.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:329](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L329) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> the constructor or the class name of the component to add

##### Examples

```js
var sprite = node.addComponent(cc.Sprite);
var test = node.addComponent("Test");
```

##### getComponent

Returns the component of supplied type if the node has one attached, null if it doesn't.<br/>
You can also get component in the node by passing in the name of the script.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:347](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L347) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
// get sprite component.
var sprite = node.getComponent(cc.Sprite);
// get custom test calss.
var test = node.getComponent("Test");
```

##### getComponents

Returns all components of supplied Type in the node.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component[]</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:371](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L371) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprites = node.getComponents(cc.Sprite);
var tests = node.getComponents("Test");
```

##### getComponentInChildren

Returns the component of supplied type in any of its children using depth first search.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:389](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L389) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprite = node.getComponentInChildren(cc.Sprite);
var Test = node.getComponentInChildren("Test");
```

##### getComponentsInChildren

Returns the components of supplied type in self or any of its children using depth first search.

| meta | description |
|------|-------------|
| Returns | <a href="../classes/Component.html" class="crosslink">Component[]</a> 
| Defined in | [cocos2d/core/components/CCComponent.js:407](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L407) |

###### Parameters
- `typeOrClassName` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">Function</a> &#124; <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/String" class="crosslink external" target="_blank">String</a> 

##### Examples

```js
var sprites = node.getComponentsInChildren(cc.Sprite);
var tests = node.getComponentsInChildren("Test");
```

##### _getLocalBounds

If the component's bounding box is different from the node's, you can implement this method to supply
a custom axis aligned bounding box (AABB), so the editor's scene view can perform hit test properly.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:427](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L427) |

###### Parameters
- `out_rect` <a href="../classes/Rect.html" class="crosslink">Rect</a> the Rect to receive the bounding box


##### onRestore

onRestore is called after the user clicks the Reset item in the Inspector's context menu or performs
an undo operation on this component.<br/>
<br/>
If the component contains the "internal state", short for "temporary member variables which not included<br/>
in its CCClass properties", then you may need to implement this function.<br/>
<br/>
The editor will call the getset accessors of your component to record/restore the component's state<br/>
for undo/redo operation. However, in extreme cases, it may not works well. Then you should implement<br/>
this function to manually synchronize your component's "internal states" with its public properties.<br/>
Once you implement this function, all the getset accessors of your component will not be called when<br/>
the user performs an undo/redo operation. Which means that only the properties with default value<br/>
will be recorded or restored by editor.<br/>
<br/>
Similarly, the editor may failed to reset your component correctly in extreme cases. Then if you need<br/>
to support the reset menu, you should manually synchronize your component's "internal states" with its<br/>
properties in this function. Once you implement this function, all the getset accessors of your component<br/>
will not be called during reset operation. Which means that only the properties with default value<br/>
will be reset by editor.

This function is only called in editor mode.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:440](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L440) |



##### schedule

Schedules a custom selector.<br/>
If the selector is already scheduled, then the interval parameter will be updated without scheduling it again.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:542](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L542) |

###### Parameters
- `callback` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> The callback function
- `interval` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> Tick interval in seconds. 0 means tick every frame.
- `repeat` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The selector will be executed (repeat + 1) times, you can use cc.macro.REPEAT_FOREVER for tick infinitely.
- `delay` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The amount of time that the first tick will wait before execution.

##### Examples

```js
var timeCallback = function (dt) {
  cc.log("time: " + dt);
}
this.schedule(timeCallback, 1);
```

##### scheduleOnce

Schedules a callback function that runs only once, with a delay of 0 or larger.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:579](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L579) |

###### Parameters
- `callback` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> A function wrapped as a selector
- `delay` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Number" class="crosslink external" target="_blank">Number</a> The amount of time that the first tick will wait before execution.

##### Examples

```js
var timeCallback = function (dt) {
  cc.log("time: " + dt);
}
this.scheduleOnce(timeCallback, 2);
```

##### unschedule

Unschedules a custom callback function.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:596](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L596) |

###### Parameters
- `callback_fn` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Function" class="crosslink external" target="_blank">function</a> A function wrapped as a selector

##### Examples

```js
this.unschedule(_callback);
```

##### unscheduleAllCallbacks

unschedule all scheduled callback functions: custom callback functions, and the 'update' callback function.<br/>
Actions are not affected by this method.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/components/CCComponent.js:612](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/components/CCComponent.js#L612) |


##### Examples

```js
this.unscheduleAllCallbacks();
```

##### destroy

Destroy this Object, and release all its own references to other objects.<br/>
Actual object destruction will delayed until before rendering.
From the next frame, this object is not usable any more.
You can use cc.isValid(obj) to check whether the object is destroyed before accessing it.

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 
| Defined in | [cocos2d/core/platform/CCObject.js:296](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L296) |


##### Examples

```js
obj.destroy();
```

##### _destruct

Clear all references in the instance.

NOTE: this method will not clear the getter or setter functions which defined in the instance of CCObject.
      You can override the _destruct method if you need, for example:
      _destruct: function () {
          for (var key in this) {
              if (this.hasOwnProperty(key)) {
                  switch (typeof this[key]) {
                      case 'string':
                          this[key] = '';
                          break;
                      case 'object':
                      case 'function':
                          this[key] = null;
                          break;
              }
          }
      }

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:428](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L428) |



##### _onPreDestroy

Called before the object being destroyed.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:461](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L461) |



##### _serialize

The customized serialization for this object. (Editor Only)

| meta | description |
|------|-------------|
| Returns | <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">object</a> 
| Defined in | [cocos2d/core/platform/CCObject.js:486](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L486) |

###### Parameters
- `exporting` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Boolean" class="crosslink external" target="_blank">Boolean</a> 


##### _deserialize

Init this object from the custom serialized data.

| meta | description |
|------|-------------|
| Defined in | [cocos2d/core/platform/CCObject.js:496](https://github.com/cocos-creator/engine/blob/79542d65dc19c8718cb54c9afa022e8f91855f48/cocos2d/core/platform/CCObject.js#L496) |

###### Parameters
- `data` <a href="https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Object" class="crosslink external" target="_blank">Object</a> the serialized json data
- `ctx` _Deserializer 



