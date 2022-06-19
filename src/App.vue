<script setup lang="ts">
import { ref } from 'vue'
import TheHeader from './components/TheHeader.vue'
import TheInput from './components/TheInput.vue'

const valor = ref('')
const data = ref('')
const observacao = ref('')
</script>

<template>
  <TheHeader />

  <div class="container mx-auto">
    <div class="grid grid-cols-4 mt-8 gap-4 content-end grid-rows-1">
      <div>
        <label
          for="txtValor"
          class="block"
        >
          Valor
        </label>
        <TheInput
          id="txtValor"
          type="text"
          v-model="valor"
          name="txtValor"
          placeholder="Valor:"
          class="min-w-full"
        />
      </div>

      <div>
        <label
          for="txtData"
          class="block"
        >
          Data
        </label>
        <TheInput
          id="txtData"
          type="text"
          v-model="data"
          name="txtData"
          placeholder="Data:"
          class="min-w-full"
        />
      </div>

      <div>
        <label
          for="txtObservacao"
          class="block"
        >
          Observação
        </label>
        <TheInput
          id="txtObservacao"
          type="text"
          v-model="observacao"
          name="txtObservacao"
          placeholder="Observação:"
          class="min-w-full"
        />
      </div>

      <button class="border border-blue-800 pt-2 py-2 min-w-full rounded-md bg-blue-600 text-white">
        Salvar
      </button>
    </div>
  </div>
</template>

<style>
</style>
