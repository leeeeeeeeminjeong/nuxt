<script setup>

  import { ref } from 'vue'

  import CounterComp from '../components/CounterComp.vue'
  import InputForm from '../components/InputForm.vue'

  const resultMsg = ref('')

</script>

<template>
  <div>
    <CounterComp />
    <InputForm v-model="resultMsg"/>

    <p> {{ resultMsg }}</p>
  </div>
</template>

<style scoped>

</style>