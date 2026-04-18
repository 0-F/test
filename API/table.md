# table
<!-- toc -->
# yalu.table<a name="yalu.table"></a>  

---  
## Functions
### deepCopy(orig : [`table`](../API/builtins/table.md), cache : [`table`](../API/builtins/table.md)[`?`](../API/builtins/nil.md))<a name="deepCopy"></a>
`->`copy : [`any`](../API/builtins/any.md)  

> Recursively copies a table and all its nested tables.
> Handles circular references using an internal cache.
### flatten(list : [`table`](../API/builtins/table.md))<a name="flatten"></a>
`->`table : [`table`](../API/builtins/table.md)  

> Merges an array of tables into a single flat table.<br>
> Iterates through each sub-table and copies all key-value pairs into a new result table.<br>
> If multiple sub-tables share the same key, the value from the later table overwrites the earlier one.<br>
> 
> ### Usage
> ```lua
> local list = {
>     { id = 1, type = "actor" },
>     { name = "Gnomon", id = 500 }
> }
> local result = M.flatten(list)
> -- result is { id = 500, type = "actor", name = "Gnomon" }
> ```
### includes(list : [`table`](../API/builtins/table.md), value : [`any`](../API/builtins/any.md))<a name="includes"></a>
`->`[`boolean`](../API/builtins/boolean.md)  

### merge(t1 : table<<K>, <V>>, t2 : table<<K>, <V>>)<a name="merge"></a>
`->`t1 : table<<K>, <V>>  

> Merge the contents of the second table into the first one.<br>
> If both tables share the same key, the value from the second table (t2) overwrites the first (t1).  



