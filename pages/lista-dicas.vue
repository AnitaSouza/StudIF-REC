<template>
  <div>
    <ul>
      <li v-for="dica in listaDicas" :key="dica.id">
        <NuxtLink v-bind:to="`tela-dica/${dica.id}`">
          {{ dica.titulo }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      listaDicas: [
        {
          id: 0,
          titulo: 'Como aguentar o prof Luiz',
          descricao:
            'Leia, mas escreva tambem. O estudo feito só por meio da leitura não é tão eficiente. O estudante pode se pegar facilmente distraido no  decorrer das páginas. Por isso, escreva! Faça esquemas, transcreva partes importantes e organize resumos. Quem escreve consegue assimilar melhor o conteúdo e tê-lo por mais tempo na mente.',
        },
        {
          id: 1,
          titulo: 'Como migrar para a mecânica',
          descricao: 'dica 2',
        },
      ],
    }
  },
}
</script>

<style>
</style>