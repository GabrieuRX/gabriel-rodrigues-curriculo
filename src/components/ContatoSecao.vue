<script setup>
defineProps({
  contato: { type: Array, required: true }
})
</script>

<template>
  <section class="contato">
    <h2 class="rotulo">Contato</h2>
    <p v-for="c in contato" :key="c.rotulo">
      <strong>{{ c.rotulo }}:</strong> {{ c.valor }}
    </p>
  </section>
</template>

<style scoped>
.contato p { font-size: 14px; line-height: 2; }
.contato strong { font-family: var(--mono); font-weight: 700; }
</style>