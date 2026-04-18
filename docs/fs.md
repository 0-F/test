# fs
<!-- toc -->
# yalu.fs<a name="yalu.fs"></a>  

---  
## Functions
### copyFile(source : [`string`](../API/builtins/string.md), destination : [`string`](../API/builtins/string.md))<a name="copyFile"></a>
`->`success : [`boolean`](../API/builtins/boolean.md), errorMessage : [`string`](../API/builtins/string.md) | [`nil`](../API/builtins/nil.md)  

> Copy a file from a source path to a destination path.
### doesDirExist(path : [`string`](../API/builtins/string.md))<a name="doesDirExist"></a>
`->`exists : [`boolean`](../API/builtins/boolean.md)  

> Check if a directory exists at the specified path.
### doesFileExist(fileName : [`string`](../API/builtins/string.md))<a name="doesFileExist"></a>
`->`exists : [`boolean`](../API/builtins/boolean.md)  

> Check if a file exists and is readable at the specified path.
### getDirectoryList(directory : [`string`](../API/builtins/string.md), filter : [`string`](../API/builtins/string.md)[`?`](../API/builtins/nil.md))<a name="getDirectoryList"></a>
`->`dirList : [`string`](../API/builtins/string.md)[]  

> Retrieve a list of directories within a root directory, filtered by a pattern.<br>
> Supports both Windows (cmd) and Linux/WSL (bash).
### getFileList(directory : [`string`](../API/builtins/string.md), filter : [`string`](../API/builtins/string.md))<a name="getFileList"></a>
`->`fileList : [`string`](../API/builtins/string.md)[]  

> Retrieve a list of files within a directory and its subdirectories, filtered by a pattern.<br>
> Supports both Windows (cmd) and Linux/WSL (bash).
### joinPaths(...[`string`](../API/builtins/string.md) | [`number`](../API/builtins/number.md))<a name="joinPaths"></a>
`->`[`string`](../API/builtins/string.md)  

> Joins multiple path components into a single normalized path.
### normalizePath(path : [`string`](../API/builtins/string.md))<a name="normalizePath"></a>
`->`[`string`](../API/builtins/string.md)  

> Normalizes a path string to use single forward slashes.
### readFile(fileName : [`string`](../API/builtins/string.md))<a name="readFile"></a>
`->`content : [`string`](../API/builtins/string.md) | [`nil`](../API/builtins/nil.md), errorMessage : [`string`](../API/builtins/string.md) | [`nil`](../API/builtins/nil.md)  

> Read the entire content of a file into a string.  



