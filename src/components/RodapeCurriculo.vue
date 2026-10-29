<template>
  <footer class="rodape">
    Copyright 2026 - todos os direitos reservados
  </footer>
</template>

<style scoped>
.rodape {
  grid-column: 1 / 9;
  border-top: 1px solid var(--linha);
  padding-top: 32px;
  font: 400 12px/1 var(--mono);
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--cinza-claro);
}

@media (max-width: 900px) {
  .rodape { grid-column: 1 / -1; }
}
</style>