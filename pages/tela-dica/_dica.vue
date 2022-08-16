<template>
  <div>
    <barraNav></barraNav>
    <b-container class="container">
      <img src="lampada.webp" width="320" height="205" />
      <center><p>Dica do dia</p></center>

      <b-container class="DicadoDia">
        <h5>{{ listaDicas[dica].titulo }}</h5>
        <p>
          {{ listaDicas[dica].descricao }}
        </p>
      </b-container>

      <b-container class="BancodeDicas">
        <center><p>Banco de Dicas</p></center>
      </b-container>
      <b-container class="AddDicas">
        <center><p>+ Adicionar Dicas</p></center>
      </b-container>
    </b-container>
  </div>
</template>

<script>
import barraNav from '~/components/barraNav.vue'
export default {
  name: 'IndexPage',
  components: { barraNav },
  async asyncData({ route }) {
    const { dica } = await route.params
    return { dica }
  },
  data() {
    return {
      listaDicas: [
        {
          id: 0,
          titulo: 'Como aguentar o prof Luiz',
          descricao:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Morbi non arcu risus quis. Nec feugiat in fermentum posuere urna nec tincidunt praesent. Nam libero justo laoreet sit amet cursus sit.',
        },
        {
          id: 1,
          titulo: 'Como migrar para a mecânica',
          descricao:
            'Neque convallis a cras semper. Aenean vel elit scelerisque mauris. Et netus et malesuada fames ac turpis egestas. Pharetra pharetra massa massa ultricies mi quis. Dis parturient montes nascetur ridiculus mus.',
        },
      ],
    }
  },
}
</script>
<style>
html,
body {
  height: 100%;
  width: 100%;
  background-color: rgb(255, 255, 255);
}
.container img {
  max-width: 200px;
  display: block;
  margin: 0 auto;
}
.DicadoDia,
.BancodeDicas,
.AddDicas {
  background-color: #c9e9af;
}
</style>
