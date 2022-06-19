<template>
  <input
    :type="types"
    :value="modelValue"
    :name="name"
    :id="id"
    :placeholder="placeholder"
    class="border p-1 rounded-md"
    @input="$emit('update:modelValue', $event.target.value)"
  >
</template>

<script setup lang="ts">
  import { computed } from 'vue'

  const props = defineProps({
    type: { type: String, required: true, default: 'text' },
    name: { type: String, required: false, default: '' },
    id: { type: String, required: false, default: '' },
    placeholder: { type: String, required: false, default: '' },
    modelValue: { type: String, required: false, default: '' }
  })

  const typesInput = ['text', 'number']

  const types = computed(() => {
    if (typesInput.includes(props.type)) {
      return props.type
    }

    return 'text'
  })
</script>

<style scoped>

</style>
