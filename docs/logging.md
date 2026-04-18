# logging
<!-- toc -->
# yalu.logging<a name="yalu.logging"></a>  
## Constants
### logLevel<a name="logLevel"></a>
> ```lua
> "ALL" | "TRACE" | "DEBUG" | "INFO" | "WARN" | "ERROR" | "FATAL" | "OFF"
> ```
  

---  
## Functions
### new(name : [`string`](../API/builtins/string.md), level : [`yalu.logging.logLevel`](../API/logging.md#yalu.logging.logLevel)[`?`](../API/builtins/nil.md), outputFunc : [`function`](../API/builtins/function.md)[`?`](../API/builtins/nil.md), outputErrFunc : [`function`](../API/builtins/function.md)[`?`](../API/builtins/nil.md))<a name="new"></a>
`->`logger : [`yalu.logging.logger`](../API/types.md#yalu.logging.logger)  

> Create a new logger instance or return the existing one.
### `getInstance()`<a name="getInstance"></a>
`->`[`yalu.logging.logger`](../API/types.md#yalu.logging.logger)  

> Get the current logger instance or throw an error if not initialized.<br>
> This ensures that the logger is created via logging.new() before use.  



