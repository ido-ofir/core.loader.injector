# core.loader.injector

loads 'dependencies' from plugin definition

related to <a href="https://github.com/ido-ofir/core.plugin.injector">core.plugin.injector</a>

```js
let core = new require('core.constructor')();
 
core.plugin(
    require('core.plugin.injector'),
    require('core.loader.injector'),
);

// plugins can now declare actions on the plugin definition object:
core.plugin({
    name: 'test',
    dependencies: ['imports.React'],
    init(){
         
        // init function will only run when all dependencies have loaded
        let { React } = core.imports;
    }
});
```
