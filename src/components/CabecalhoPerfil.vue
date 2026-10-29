<script setup>
defineProps({
  perfil: { type: Object, required: true }
})
</script>

<template>
  <header class="topo">
    <div class="logo">{{ perfil.iniciais }}</div>
    <div>
      <h1 class="nome">{{ perfil.nome }}</h1>
      <p class="cargo">{{ perfil.cargo }}</p>
    </div>
  </header>
</template>

<style scoped>
.topo {
  display: flex;
  align-items: center;
  gap: 32px;
  margin-bottom: 64px;
}
.logo {
  width: 120px;
  height: 120px;
  background: var(--amarelo);
  display: grid;
  place-items: center;
  font-weight: 700;
  font-size: 48px;
  line-height: 1;
}
.nome  { font: 600 20px/1.4 var(--mono); }
.cargo { font: 400 16px/1.4 var(--mono); color: var(--cinza); }

@media (max-width: 900px) {
  .topo { flex-direction: column; align-items: flex-start; }
}
</style>