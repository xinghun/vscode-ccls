# ccls-plus

This plugin is forked from [vscode-ccls](https://github.com/MaskRay/vscode-ccls) and adds some features, fixes some bugs.

This is the Visual Studio Code extension for [ccls](https://github.com/MaskRay/ccls),
 a C/C++/ObjC language server supporting cross references, hierarchies, completion and semantic highlighting.


## Release Notes

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
