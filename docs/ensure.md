# ensure
<!-- toc -->
# yalu.ensure<a name="yalu.ensure"></a>  

---  
## Functions
### arg(index : [`number`](../API/builtins/number.md), value : [`any`](../API/builtins/any.md))<a name="arg"></a>
`->`[`yalu.ensure.argValidator`](../API/ensure.md#yalu.ensure.argValidator)  
  



# yalu.ensure.argValidator<a name="yalu.ensure.argValidator"></a>  

---  
## Properties
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.
### is([*self*](../API/builtins/self.md), expectedType : type)<a name="is"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks the exact Lua type and switches to a type-specific validator when available.
> 
> ```lua
> expectedType:
>     | "nil"
>     | "number"
>     | "string"
>     | "boolean"
>     | "table"
>     | "function"
>     | "thread"
>     | "userdata"
> ```
### isOneOfTypes([*self*](../API/builtins/self.md), ...type)<a name="isOneOfTypes"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Accepts a value whose type matches any of the provided type names.<br>
> ### Usage:
> ```lua
> ensure.arg(1, "a"):isOneOfTypes("string", "number")
> ```
> 
> 
> ```lua
> ...(param):
>     | "nil"
>     | "number"
>     | "string"
>     | "boolean"
>     | "table"
>     | "function"
>     | "thread"
>     | "userdata"
> ```
### isBoolean([*self*](../API/builtins/self.md))<a name="isBoolean"></a>
`->`[`yalu.ensure.booleanValidator`](../API/ensure.md#yalu.ensure.booleanValidator)  

> Validates that the argument is a boolean and transitions to boolean-specific methods.
### isFunction([*self*](../API/builtins/self.md))<a name="isFunction"></a>
`->`[`yalu.ensure.functionValidator`](../API/ensure.md#yalu.ensure.functionValidator)  

> Validates that the argument is a function and transitions to function-specific methods.
### isNumber([*self*](../API/builtins/self.md))<a name="isNumber"></a>
`->`[`yalu.ensure.numberValidator`](../API/ensure.md#yalu.ensure.numberValidator)  

> Validates that the argument is a number and transitions to number-specific methods.
### isString([*self*](../API/builtins/self.md))<a name="isString"></a>
`->`[`yalu.ensure.stringValidator`](../API/ensure.md#yalu.ensure.stringValidator)  

> Validates that the argument is a string and transitions to string-specific methods.
### isTable([*self*](../API/builtins/self.md))<a name="isTable"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Validates that the argument is a table and transitions to table-specific methods.
### isUserdata([*self*](../API/builtins/self.md))<a name="isUserdata"></a>
`->`[`yalu.ensure.userdataValidator`](../API/ensure.md#yalu.ensure.userdataValidator)  

> Validates that the argument is a userdata and transitions to userdata-specific methods.  



# yalu.ensure.base<a name="yalu.ensure.base"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.base`](../API/ensure.md#yalu.ensure.base)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>  



# yalu.ensure.baseValidator<a name="yalu.ensure.baseValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.  



# yalu.ensure.booleanValidator<a name="yalu.ensure.booleanValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.
### isTrue([*self*](../API/builtins/self.md))<a name="isTrue"></a>
`->`[`yalu.ensure.booleanValidator`](../API/ensure.md#yalu.ensure.booleanValidator)  

> Checks if the boolean is exactly true.
### isFalse([*self*](../API/builtins/self.md))<a name="isFalse"></a>
`->`[`yalu.ensure.booleanValidator`](../API/ensure.md#yalu.ensure.booleanValidator)  

> Checks if the boolean is exactly false.  



# yalu.ensure.functionValidator<a name="yalu.ensure.functionValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.  



# yalu.ensure.numberValidator<a name="yalu.ensure.numberValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.
### isPositive([*self*](../API/builtins/self.md))<a name="isPositive"></a>
`->`[`yalu.ensure.numberValidator`](../API/ensure.md#yalu.ensure.numberValidator)  

> Checks if the number is strictly greater than 0.
### isNonNegative([*self*](../API/builtins/self.md))<a name="isNonNegative"></a>
`->`[`yalu.ensure.numberValidator`](../API/ensure.md#yalu.ensure.numberValidator)  

> Checks if the number is greater than or equal to 0.
### isNegative([*self*](../API/builtins/self.md))<a name="isNegative"></a>
`->`[`yalu.ensure.numberValidator`](../API/ensure.md#yalu.ensure.numberValidator)  

> Checks if the number is strictly less than 0.
### isZero([*self*](../API/builtins/self.md))<a name="isZero"></a>
`->`[`yalu.ensure.numberValidator`](../API/ensure.md#yalu.ensure.numberValidator)  

> Checks if the value is exactly 0.  



# yalu.ensure.stringValidator<a name="yalu.ensure.stringValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.
### isNotEmpty([*self*](../API/builtins/self.md))<a name="isNotEmpty"></a>
`->`[`yalu.ensure.stringValidator`](../API/ensure.md#yalu.ensure.stringValidator)  

> Checks if the string is not empty ("").
### isEmpty([*self*](../API/builtins/self.md))<a name="isEmpty"></a>
`->`[`yalu.ensure.stringValidator`](../API/ensure.md#yalu.ensure.stringValidator)  

> Checks if the string is exactly empty ("").  



# yalu.ensure.tableValidator<a name="yalu.ensure.tableValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.
### isEmpty([*self*](../API/builtins/self.md))<a name="isEmpty"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Checks if the table is empty.
### isNotEmpty([*self*](../API/builtins/self.md))<a name="isNotEmpty"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Checks if the table is not empty.
### hasKey([*self*](../API/builtins/self.md), key : [`any`](../API/builtins/any.md))<a name="hasKey"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Checks if the table contains the provided key.
### hasKeys([*self*](../API/builtins/self.md), ...[`any`](../API/builtins/any.md))<a name="hasKeys"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Checks if the table contains all provided keys.
### hasValue([*self*](../API/builtins/self.md), value : [`any`](../API/builtins/any.md))<a name="hasValue"></a>
`->`[`yalu.ensure.tableValidator`](../API/ensure.md#yalu.ensure.tableValidator)  

> Checks if the table contains the provided value.  



# yalu.ensure.userdataValidator<a name="yalu.ensure.userdataValidator"></a>  

---  
## Properties
### value : [`any`](../API/builtins/any.md)<a name="value"></a>
### index : [`number`](../API/builtins/number.md)<a name="index"></a>
### __index : [`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)<a name="__index"></a>
  

---  
## Functions
### raiseError([*self*](../API/builtins/self.md), expected : [`string`](../API/builtins/string.md))<a name="raiseError"></a>
### raiseTypeError([*self*](../API/builtins/self.md), typeExpected : [`string`](../API/builtins/string.md))<a name="raiseTypeError"></a>
### raiseConstraintError([*self*](../API/builtins/self.md), valueExpected : [`string`](../API/builtins/string.md))<a name="raiseConstraintError"></a>
### isFalsy([*self*](../API/builtins/self.md))<a name="isFalsy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is falsy (nil or false).
### isTruthy([*self*](../API/builtins/self.md))<a name="isTruthy"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Checks if the value is truthy (not nil and not false).
### validate([*self*](../API/builtins/self.md), condition : [`boolean`](../API/builtins/boolean.md) | (value : [`any`](../API/builtins/any.md)) `->` [`boolean`](../API/builtins/boolean.md))<a name="validate"></a>
`->`[`yalu.ensure.baseValidator`](../API/ensure.md#yalu.ensure.baseValidator)  

> Validates that the value satisfies a boolean or predicate function.<br>
> If a predicate is provided, it is called with the current value.  



