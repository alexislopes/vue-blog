<template>
  <div class="text-center">
    <div class="card" style="width: 18rem;">
  <img class="card-img-top" src="https://static.fraseamor.com.br/content/assetz/uploads/2018/10/339-imagens-e-frases-as-mais-legais-de-bom-dia-frases-e-mensagens-legais-legais.jpg" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">{{postagens[0].autor}}</h5>
    <!--<p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>-->
    <a href="#" class="btn btn-primary">ver mais</a>
  </div>
</div>
  </div>
</template>

<script>
  export default {
      data() {
        return {
          titulo: "faker.name.title()",
          autor: this.$faker().name.findName(),
          chamada: "Aprenda a desenhar",
          texto: ""
        }
      }
  }
</script>
