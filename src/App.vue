<template>
  <section class="container">
    <h2>{{ user.name }}</h2>
    <h3>{{ user.age }}</h3>
    <button @click="setAge">Change Age</button>
  </section>
</template>

<script>
import { reactive } from 'vue';

export default {
  setup() {
    // const uName = ref('Katrina');
    // const uAge = ref(37);

    const user = reactive({
      name: 'Katrina',
      age: 37,
    });

    // storing a pointer function in this set object below
    function setNewAge() {
      user.age = 38;
    }

    return { user: user, setAge: setNewAge };

    // setTimeout(function() {
    //   user.name = 'Kat';
    //   user.age = 32;
    // }, 2000);

    // return { user: user };

  }
  // data() {
  //   return {
  //     userName: 'Katrina',
  //   };
  // },
};
</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>