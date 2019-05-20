<template>
<div id="container">
  <div class="text-center" v-for="postagem in postagens" :key="postagem.id">
    <div class="card" style="width: 18rem;">
      <img class="card-img-top" src="https://static.fraseamor.com.br/content/assetz/uploads/2018/10/339-imagens-e-frases-as-mais-legais-de-bom-dia-frases-e-mensagens-legais-legais.jpg" alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">{{postagem.titulo}}</h5>
            <p class="card-text">{{postagem.chamada}}</p>
              <a href="#" class="btn btn-primary">ver mais</a>
        </div>
    </div>  
  </div>
</div>
</template>

<script>
  export default {
    data() {
      return {
        postagens: [
          {
            titulo: 'Como desenhar',
            autor: "João",
            chamada: "Aprenda a desenhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },
          {
            titulo: 'Como cozinhar',
            autor: "Pedro",
            chamada: "Aprenda a cozinhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },
          {
            titulo: 'Como desenhar',
            autor: "João",
            chamada: "Aprenda a desenhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },
          {
            titulo: 'Como desenhar',
            autor: "João",
            chamada: "Aprenda a desenhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },
          {
            titulo: 'Como desenhar',
            autor: "João",
            chamada: "Aprenda a desenhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },{
            titulo: 'Como desenhar',
            autor: "João",
            chamada: "Aprenda a desenhar",
            texto: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras non ex eu leo rutrum vestibulum. Etiam ut orci mollis, egestas mi sit amet, congue elit. Duis a lacinia dui. Nunc."
          },
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

  .card {
    margin: .5em
  }

</style>
