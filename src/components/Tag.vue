<template>
  <div class="tag" @click="emits('onDelete', tag)">
    <span>
      {{ tag }}
    </span>
    <span class="cross">❌</span>
  </div>
</template>

<script setup lang="ts">
interface Props {
  tag: string
}

defineProps<Props>()
const emits = defineEmits(['onDelete'])
</script>

<style scoped>
.tag {
  display: inline-flex;
  user-select: none;
  align-items: center;
  justify-content: center;
  padding: 5px 10px;
  border-radius: 3px;
  background-color: #1a1a1a;
}

.tag:hover {
  background-color: #2b2b2b;
}

.tag .cross {
  margin-left: 5px;
}
</style>