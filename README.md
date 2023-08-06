# The Composition API

## Set Up
``npm install``

``npm run serve``

## Learning Journey

**Reactive Values with ref()**

<img src="images/reactiveValue.png" width=500 />

* Vue automatically read the value

```
could be replaced with:

<script setup>
import { ref } from 'vue';
 
const uName = ref('Maximilian');
 
setTimeout(function() {
  uName.value = 'Max';
}, 2000);
</script>
```

* Learn more about <script setup>:  
https://vuejs.org/api/sfc-script-setup.html

* ref() works with any kind of value
* reactive only works with objects

<img src="images/reactive.png" width=500 />

## Managing Reactive Data 

Options API vs Composition API in Vue.

Define in set up and then expose in the template. 