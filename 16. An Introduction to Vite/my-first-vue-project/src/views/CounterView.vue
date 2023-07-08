<script setup>
// import {counter} from "@/stores/CounterStore";

import {useCounterStore} from "@/stores/CounterStore";
let counter = useCounterStore();
</script>

<template>
  <div>
    <h1>{{ counter.count }}</h1>

<!--    <button @click="counter.count++">Increment</button>-->
<!--    <button @click="counter.increment()">Increment</button>-->

    <button
        @click="counter.increment()"
        :disabled="! counter.remaining"
    >
      Increment ({{ counter.remaining  }} Remaining)
    </button>

  </div>
</template>