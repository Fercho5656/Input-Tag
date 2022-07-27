<template>
  <kbd>
    <slot />
  </kbd>
</template>

<script setup lang="ts">
</script>

<style scoped>
kbd {
  font-family: Consolas, "Lucida Console", monospace;
  display: inline-block;
  border-radius: 3px;
  padding: 0px 4px;
  box-shadow: 1px 1px 1px #777;
  margin: 2px;
  font-size: small;
  vertical-align: text-bottom;
  background: #eee;
  font-weight: 500;
  color: #555;
  font-variant: small-caps;
  font-weight: 600;

  /* This two work */
  /* letter-spacing: 0.5px; */
  letter-spacing: 1px;


  /* Prevent selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

kbd:hover,
kbd:hover * {
  color: black;
}

kbd:active,
kbd:active * {
  color: black;
  box-shadow: 1px 1px 0px #ddd inset;
}
</style>