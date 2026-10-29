<script setup>
import { perfil, experiencias, educacao, contato } from './data/curriculo'
import CabecalhoPerfil from './components/CabecalhoPerfil.vue'
import ListaSecao from './components/ListaSecao.vue'
import ContatoSecao from './components/ContatoSecao.vue'
import RodapeCurriculo from './components/RodapeCurriculo.vue'
</script>

<template>
  <div class="pagina">
    <CabecalhoPerfil :perfil="perfil" />

    <div class="grade">
      <main class="principal">
        <section>
          <p>{{ perfil.resumo }}</p>
        </section>

        <ListaSecao titulo="Experiências Profissionais" :itens="experiencias" />
      </main>

      <aside class="lateral">
        <ListaSecao titulo="Educação" :itens="educacao" />
        <ContatoSecao :contato="contato" />
      </aside>

      <RodapeCurriculo />
    </div>
  </div>
</template>
