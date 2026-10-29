<script setup>
defineProps({
  titulo: { type: String, required: true },
  itens: { type: Array, default: () => [] }
})
</script>

<template>
  <section>
    <h2 class="rotulo">{{ titulo }}</h2>

    <p v-if="!itens.length" class="vazio">Nenhum item cadastrado.</p>

    <article v-for="item in itens" :key="item.titulo" class="item">
      <h3>{{ item.titulo }}</h3>
      <p class="subtitulo">{{ item.subtitulo }}</p>
      <p>{{ item.texto }}</p>
    </article>
  </section>
</template>

<style scoped>
.item { margin-bottom: 40px; }
.item h3 { font-size: 16px; font-weight: 700; line-height: 1.6; }
.item .subtitulo { font: 400 16px/1.6 var(--mono); color: var(--cinza); }
.item p { font-size: 16px; }
.vazio { color: var(--cinza); }
</style>