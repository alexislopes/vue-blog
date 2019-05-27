<template>
<div class="ui items">
  <div class="item" v-for="post in postagens" :key="post.id">
    <div class="image">
      <img :src="post.imagem">
    </div>
    <div class="content">
      <a class="header">{{post.titulo}}</a>
      <div class="meta">
        <span>{{post.chamada}}</span>
      </div>
      <div class="description">
        <p></p>
      </div>
      <div class="extra">
        {{post.autor}}
      </div>
    </div>
  </div>
</div>
</template>

<script>
  import faker from 'faker';
  faker.locale = 'pt_BR';

  export default {
    data() {
      return {
        postagens: [
          {
            titulo: faker.name.title(),
            imagem: faker.image.image(),
            autor: faker.name.findName(),
            chamada: faker.lorem.sentence(),
            texto: faker.lorem.paragraph()
          },
          {
            titulo: faker.name.title(),
            imagem: faker.image.image(),
            autor: faker.name.findName(),
            chamada: faker.lorem.sentence(),
            texto: faker.lorem.paragraph()
          },
          {
            titulo: faker.name.title(),
            imagem: faker.image.image(),
            autor: faker.name.findName(),
            chamada: faker.lorem.sentence(),
            texto: faker.lorem.paragraph()
          },
          {
            titulo: faker.name.title(),
            imagem: faker.image.image(),
            autor: faker.name.findName(),
            chamada: faker.lorem.sentence(),
            texto: faker.lorem.paragraph()
          },
          {
            titulo: faker.name.title(),
            imagem: faker.image.image(),
            autor: faker.name.findName(),
            chamada: faker.lorem.sentence(),
            texto: faker.lorem.paragraph()
          }
        ]
      }
    }
  }
  
</script>

<style scoped>
  #container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    width: 100%;
    background-color: brown;
  }

  .item {
    float: center;
    background-color: black
  }

  .items {
    margin: 2rem 0 0 2rem;
    display: grid;
  }

</style>
