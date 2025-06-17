<script setup>
import { ref, defineEmits } from 'vue'

const inputValue = ref('')

const emit = defineEmits(['update:modelValue'])

function sendMsg(e){
  emit('update:modelValue', e.target.value);
}
</script>

<template>
  <input v-model="inputValue" placeholder="input text..!" @input="sendMsg">
</template>

<style scoped>

</style>