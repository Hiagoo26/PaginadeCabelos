<template>
     <div class="slidebar">
        <div class="slides" :style="{ transform: `translateX(${-num * 100}%)` }">
           <div class="slide" v-for="(imagem, i) in imagens" :key="i">
              <img :src="imagem" alt="Produto clear man">
              <p class="legenda">{{ legendas[i] }}</p>
            </div>
        </div>
          <button class="antes" @click="antes">&lt;</button>
          <button class="depois" @click="dps">&gt;</button>
      </div>
</template>

<script>

  export default {
    nome: 'Imagens',
    data(){
      return {
        imagens: [
          require('@/assets/clear.jpeg'),
          require('@/assets/hair.jpeg'),
          require('@/assets/kera.jpeg')
        ],
        num: 0,
        legendas: [
          'Novos Shampoos Clear Man, Vini Jr e Haaland',
          'Fashion Hair - Seu cabelo em bons cuidados',
          'Keraton lança nova linha Neon'
        ],
        index: 0,
      }
    },
    methods: {
      antes() {
        this.num = (this.num - 1 + this.imagens.length) %this.imagens.length
      },
      dps() {
        this.num = (this.num + 1) % this.imagens.length
      }
    },
    mounted() {
      setInterval(() => this.dps(), 3000)
    }
  }
</script>

<style scoped>
.slidebar {
    flex: 1;
    position: relative;
    width: 500px;
    height: 300px;
    overflow: hidden;
    border-radius: 10px;
    align-items: center;
    align-content: center;
    border: 2px;
    background: #3e4042;
    padding-right: 40px;
}

.slides {
    display: flex;
    transition: transform 1.5s ease-in-out
}

.slide {
    min-width: 100%;
    position: relative;
    object-fit: cover;
}

img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    max-width: 100%;
    max-height: 300px;
    display: block;
    margin: auto;

}

.legenda {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.7);
  color: #9400d3;
  font-size: 15px;
  text-align: center;
  padding: 5px;
}

.antes{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: #3e4042;
    color: #9400d3;
    border: none;
    padding: 10px;
    left: 10px;
}
.depois{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: #3e4042;
    color: #9400d3;
    border: none;
    padding: 10px;
    right: 10px;
}

</style>