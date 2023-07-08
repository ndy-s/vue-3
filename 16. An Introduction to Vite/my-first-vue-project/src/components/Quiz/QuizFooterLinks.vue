<template>
  <div>
<!--    <h5>{{ quiz.name }}</h5>-->
<!--    <h5>{{ key }}</h5>-->
<!--    <h5>{{ name }}</h5>-->

<!--    <button @click="changeName">{{ name }}</button>-->

        <h5>{{ state.name }}</h5>

        <button @click="state.name = 'A New Quiz Name'">Change Quiz Name</button>
    <ul>
      <li><a href="#">Get a Job</a></li>
      <li><a href="#">Contact Us</a></li>
    </ul>
  </div>
</template>

<script setup>
  // import {inject} from "vue";
  //
  // defineProps({
  //   quiz: Object
  // });
  //
  // let quiz = inject('quiz');
  //
  // let key = inject('key');
  // // let name = inject('name');
  //
  // // setTimeout(() => {
  // //   name.value = 'A New Name!';
  // // }, 2000);
  //
  // let { name, changeName } = inject('name');

  import { state } from "@/stores/quizStore";
</script>