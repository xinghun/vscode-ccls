# ccls-plus

This plugin is forked from [vscode-ccls](https://github.com/MaskRay/vscode-ccls) and adds some features, fixes some bugs.

This is the Visual Studio Code extension for [ccls](https://github.com/MaskRay/ccls),
 a C/C++/ObjC language server supporting cross references, hierarchies, completion and semantic highlighting.


## Release Notes

### 0.1.34
* add: ccls.callHierarchy and ccls.memberHierarchy support C and C++ source files

### 0.1.33
* add: New configuration `ccls.codeLens.maxFileLines` :
    * Enabling codelens in very large files can cause the editor to be very slow, use this option to limit the maximum number of lines in a file with references CodeLens enabled.
    * References CodeLens will be disabled in files with more lines than this setting. Default -1 means never disable.
    
### 0.1.32
* add: New configuration `ccls.cache.fullLoadOnInitialize` :
    * When handling an initialize request from the client, full load the cache before starting the index process. 
    * **Note**: The expired caches are also loaded. So it may be inaccurate until the index process is actually complete. 
    * The main purpose of turning this option on is to start working quickly with a less accurate (but mostly accurate) cache without waiting for the slow index process to complete.
    * **Note**: [official ccls](https://github.com/MaskRay/ccls) does not support this option, use [wallenwang's fork](https://github.com/xinghun/ccls) to support this option.

### 0.1.31
* add: New configuration `ccls.treeViews.navigateBySingleClick` :
    * By default, if a parent entry in the tree view (call/inheritance/member hiearchy) is **double** clicked, vscode will navigate to the entry. 
    * Set this option to true to navigate by **single** clicking.
    * Child entries always use single click to navigate.

### 0.1.30
* fix: Solves broken hierarchy windows (e.g. call hierarchy), where after one execution future executions fail to update the window. The fix code comes from: [adam-flynn](https://github.com/adam-flynn/vscode-ccls)


See:

* [ccls/wiki/Home](https://github.com/MaskRay/ccls/wiki/Home)
* [ccls/wiki/Visual Studio Code](https://github.com/MaskRay/ccls/wiki/Visual-Studio-Code)
* [enable SemanticTokens Rainbow](doc/enable-rainbow-colors.md)
* [ccls of wallenwang's fork](https://github.com/xinghun/ccls)
