# bv-gridview
This is a Bootstrap Vue powered replacement of a PHP gridview I made in Laravel: https://github.com/Sammaye/laravel-gridview 

**Note:** This is meant to be an example only, however, I have used it in live code as a plugin.

## Usage

You can, in Laravel, import it via `require`:
```js
Vue.use(require('BvGridview'));
```
and use it in a component:
```html
<template>
    <bv-gridview
        :id="id"
        :primary-key="primaryKey"
        :api-url="apiUrl"
        :filter-on="filterOn"
        :sort-by="sortBy"
        :sort-desc="sortDesc"
        :page="page"
        :per-page="perPage"
        :fields="fields"
    ></bv-gridview>
</template>
```

If you need a more concrete example the `example.vue` file provides a full one.

the file example also includes using grand children slots through this component. 
