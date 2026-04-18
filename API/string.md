# string
<!-- toc -->
# yalu.string<a name="yalu.string"></a>  

---  
## Functions
### stringToTable(str : [`string`](../API/builtins/string.md), separator : [`string`](../API/builtins/string.md))<a name="stringToTable"></a>
`->`table : [`table`](../API/builtins/table.md)  

> Splits a string into tokens and returns a lookup table.<br>
> Each token is used as a key in the returned table, with its 1-based index as the value.
> 
> ### Usage
> ```lua
> local res = M.stringToTable("apple,banana,cherry", ",")
> -- res will be:
> { ["apple"] = 1, ["banana"] = 2, ["cherry"] = 3 }
> ```  



