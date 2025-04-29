# Vue.js Prep Notes

## History of Vue.js (2013-2020)
- **2013**: Created by **Evan You** as a lightweight alternative to AngularJS.
- **2014**: Official release as open-source.
- **2015-2016**: Gained momentum; Vue Router and Vuex introduced.
- **2017-2018**: Vue 2.x released with virtual DOM improvements.
- **2020**: Vue 3 development began; major performance and TypeScript upgrades.

## Vue 3 CDN Link
For **Vue 3** (`vue@next` repo):
```html
<script src="https://cdn.jsdelivr.net/npm/vue@next"></script>
```
For **Vue 2** (`vue@next` repo):
```html
<script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
```
### Vue Code and Data Objects
- Data object: Holds state and is referenced in HTML via template syntax ({{ message }}).


### html
```
<div id="app">
  <p>{{ message }}</p>
</div>
<script>
  const app = Vue.createApp({ data() { return { message: "Hello!" }; } });
  app.mount("#app");
</script>
```

### v-model (Two-way Data Binding)
` Two-way binding between data and input elements.

### html
```
<input v-model="message" />
<p>{{ message }}</p>
```
### v-if vs v-show
- v-if: Renders element based on condition, removes from DOM if false.

- v-show: Always renders element but toggles visibility via display: none.

### v-else-if and v-else
- v-else-if: Follows v-if for multiple conditions.

- v-else: Default condition when v-if and v-else-if fail.

### html
```
<p v-if="x === 1">Condition 1</p>
<p v-else-if="x === 2">Condition 2</p>
<p v-else>Condition 3</p>
```
### v-cloak
Keeps element hidden until Vue finishes compiling the template.

### html
```<div v-cloak>{{ message }}</div>```







