<script setup>
  // import { ref, watch } from "vue";
  import { useStorage } from "@/composables/useStorage";

  let food = useStorage('food', 'salad');
  let age = useStorage('age', '10');

  let obj = useStorage('obj', { one: 'one' });

  setTimeout(() => {
    obj.value.one = 'CHANGED';
  }, 2000);
  // let food = ref(localStorage.getItem('food'));
  // let age = ref(localStorage.getItem('age'));
  //
  // watch(food, (val) => {
  //   write('food', val);
  // });
  // function write(key, val) {
  //   localStorage.setItem(key, val);
  // }
  //
  // setTimeout(() => {
  //   food.value = 'changed';
  // }, 2000);
</script>

<template>
  <main>
    <div class="about">
      <h1>This is an contact page</h1>

      <p>
        What is your favorite food? <input type="text" v-model="food">
      </p>

      <p>
        How old are you? <input type="text" v-model="age">
      </p>
    </div>
  </main>

</template>

<style>
@media (min-width: 1024px) {
  .contact {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
