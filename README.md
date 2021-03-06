# vue-selectbox

## Demo

[Here is a demo](https://cdn.rawgit.com/venmax/vue-selectbox/010954a2/selectbox.html)

## Basic Usage

### Common use 

The most common use case is pass options to component vue-select, and bind a model to sync values with parent.

```javascript
    Vue.component('v-selectbox', vSelectBox);

    new Vue({
        el: '#app',
        data: {
            options: [
                {id:1,label:'option 1'},
                {id:2,label:'option 2'},
                {id:3,label:'option 3'},
                {id:4,label:'option 4'}],
            selectedVal: null
        }
    })
```
```html
<v-selectbox class="v-select-box" v-bind:options="options" v-model="selectedVal"></v-selectbox>
```

### Setting Options
```html
<v-selectbox class="v-select-box" v-bind:disabled="isDisabled" v-bind:options="options" v-model="selectedVal"
                 data-default="Select" data-key-name="label" data-val-name="id"></v-selectbox>
```

Accepted options:

| Option name | value | required/default |
| ------| ------ | ------ |
| v-bind:options | array | required |
| v-model | vue data object | required |
| data-default | default select label | default: Select |
| data-key-name | option key | default: name | 
| data-val-name | option value | default: id |
| v-bind:disabled | true/false | default: false |
