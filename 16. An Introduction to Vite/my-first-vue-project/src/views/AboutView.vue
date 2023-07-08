<script setup>
  // import flash from "@/mixins/flash";
  import {useFlash} from "@/composables/useFlash";
  import {counter} from "@/stores/CounterStore";

  // export default {
  //   mixins: [flash]
  // }

  let { flash } = useFlash();
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>

    <p>
      <button @click="flash('about', 'It Works', 'info')">Click Me</button>
    </p>

    <p>
      The current count is {{ counter.count }}
    </p>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
