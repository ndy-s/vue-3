<template>
  <h1>{{ name }}</h1>

  <QuizHeader />

  <QuizQuestion />

<!--  <QuizFooter :quiz="quiz" />-->
  <QuizFooter />
</template>

<script setup>
  import QuizHeader from "@/components/Quiz/QuizHeader.vue";
  import QuizQuestion from "@/components/Quiz/QuizQuestion.vue";
  import QuizFooter from "@/components/Quiz/QuizFooter.vue";
  // import { provide, ref } from "vue";
  import { state } from "@/stores/quizStore";

  // let props = defineProps({
  //   quiz: Object
  // });

  // let name = ref("John Doe")
  //
  // provide('key', 'Hello there!!!');
  // // provide('name', name);
  //
  // provide('name', {
  //   name,
  //   changeName: () => name.value = 'Changed',
  // })
  //
  // provide('quiz', props.quiz);
</script>