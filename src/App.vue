<template>
  <h1>Input Tag</h1>
  <ul>
    <li>Write something and press <kbd-key>enter</kbd-key> to add a tag</li>
    <li>Press <kbd-key>delete</kbd-key> or <kbd-key>backspace</kbd-key> key when
      the input text is empty to delete the last tag</li>
    <li>You can also press the '❌' to delete a tag</li>
  </ul>
  <input-tag />
</template>

<script setup lang="ts">
import InputTag from './components/InputTag.vue';
import KbdKey from './components/KbdKey.vue';
</script>

<style scoped>
ul {
  text-align: left;
}
</style>