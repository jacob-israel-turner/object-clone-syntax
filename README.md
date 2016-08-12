# object-clone-syntax

## Problem

``` javascript
import { someObject } from 'some-module'

addThingToDOM('div', someObject) // Just use the whole object, even though only some properties are needed

// or

addThingToDOM('div', {a: someObject.a, b: someObject.b, c: someObject.d})  // Manually select each property

// or

const {a, b, d} = someObject

addThingToDOM('div', {a, b, d})  // Destructure, then individually insert each property
```

## Solution

New object clone syntax, with defined properties

``` javascript
import { someObject } from 'some-module'

addThingToDOM('div', [someObject]{a, b, d}) // Use a new object, which is a copy of someObject, but only with properties a, b, and d
```
