<script setup>
import { ref, defineEmits } from 'vue'

const idx = ref(0);
const emit = defineEmits(['update:modelValue'])

// const double = computed(() => idx.value * 2)

function testFunc(e){
  if(e.target.id === 'up'){
    idx.value ++
  }else{
    idx.value --
  }
  emit('update:modelValue', idx.value);
}

</script>

<template>
  <button id="up" @click="testFunc"> + </button>
  <button id="down" @click="testFunc" > - </button>
</template>

