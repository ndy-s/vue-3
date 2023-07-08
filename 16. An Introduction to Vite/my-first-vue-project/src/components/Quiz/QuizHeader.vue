<template>
  <header>
    <h1>Quiz Header</h1>
    <h1>{{ state.name }}</h1>

    <p>
      Welcome to your first quiz. How do you think you'll do?
    </p>
  </header>
</template>

<script setup>
  import {state} from "@/stores/quizStore";
</script>