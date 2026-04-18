# math
<!-- toc -->
# yalu.math<a name="yalu.math"></a>  

---  
## Functions
### isAlmostEqual(x : [`number`](../API/builtins/number.md), y : [`number`](../API/builtins/number.md), epsilon : [`number`](../API/builtins/number.md)[`?`](../API/builtins/nil.md))<a name="isAlmostEqual"></a>
`->`isClose : [`boolean`](../API/builtins/boolean.md)  

> Checks if two numbers are approximately equal within a given range.<br>
> Uses the absolute difference to determine if the values are close enough.<br>
> Default epsilon value is 0.01 if not provided.<br>
> Math symbol: ≈ (Unicode: U+2248 ALMOST EQUAL TO).
### round(x : [`number`](../API/builtins/number.md), decimalPlaces : [`number`](../API/builtins/number.md))<a name="round"></a>
`->`The : [`number`](../API/builtins/number.md)  

> Truncates a number to a specified number of decimal places.<br>
> ### Usage
> ```lua
> local val = M.round(12.3456, 3) -- val is 12.345
> ```  



