<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import useColorpicker from "../composables/useColorpicker";

export default {
  setup(){
    const {colors, message, matchColor} = useColorpicker()
    return { colors, message, matchColor };
  } 
};
</script>

<style></style>
