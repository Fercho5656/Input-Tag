<template>
  <div class="inputTags">
    <div class="tags">
      <tag v-for="tag in tags" :key="tag" :tag="tag" @on-delete="onDelete(tag)" />
    </div>
    <input type="text" v-model="value" @keyup.enter="onAdd" @keyup.delete="onPop"
      placeholder="Write something...">
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Tag from './Tag.vue'

const value = ref<string>('')
const tags = ref<string[]>([])

const onAdd = () => {
  if (value.value === '') return
  if (tags.value.includes(value.value)) return
  tags.value.push(value.value)
  value.value = ''
}

const onPop = () => {
  if (value.value !== '') return
  if (tags.value.length === 0) return
  tags.value.pop()
}

const onDelete = (tagName: string) => tags.value = tags.value.filter(tag => tag !== tagName)
</script>

<style scoped>
.inputTags {
  display: inline-flex;
  background-color: #3B3B3B;
  border-radius: 5px;
  padding: 5px;
  min-height: 30px;
}

.tags {
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-content: flex-start;
  gap: 5px;
}

input[type="text"] {
  font-size: inherit;
  border: none;
  outline: none;
  padding: 0 5px;
  border-radius: 5px;
}
</style>