<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { ref } from "vue";
import {useFlash} from "@/composables/useFlash";

let message = ref("Hello, World!");
let { flash } = useFlash();
let doSomething = () => {
  swal('Warning!', 'Doing it now!', 'warning');
};

setTimeout(() => {
  message.value = "I Have Been Changed";
}, 2000);
</script>

<template>
  <main>
    <TheWelcome />

    <p>{{ message }}</p>

    <p>
      <input type="text" v-model="message">
      <button @click="doSomething">Click me!</button>

      <button  @click="flash('test', 'It Works!')">Click another me!</button>
    </p>
  </main>
</template>
