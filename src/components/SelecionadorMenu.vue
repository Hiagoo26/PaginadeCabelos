<template>
    <div class="corcabelo">
      <h3>Selecione a Cor do seu Cabelo</h3>
      <div class="cor">
        <div v-for="(cor, i) in cores"  :key="i"
          :class="['opcoescor', { selecionada: cor === corSelecionada }]"
          @click="selecionarCor(cor)"
          :style="{ backgroundImage: `url(${cor})` }"> 
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        corSelecionada: '',
        cores: [
          require('@/assets/cabeloCastanho.webp'),
          require('@/assets/cabeloLoiro.webp'),
          require('@/assets/cabeloLoiroClaro.webp'),
          require('@/assets/cabeloPreto.webp'),
          require('@/assets/cabeloLouroEscuroVermelhoIntenso.webp'),
        ],
      };
    },
    methods: {
      selecionarCor(cor) {
        this.corSelecionada = cor;
      }
    }
  };
  </script>


<style scoped>
.corcabelo {
    color: white;
    width: 50%;
    max-width: 600px;
    margin: 0%;
    text-align: center;
    font-size: 26px;
    position: relative;
}


.cor {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;
  background-color: #9400d3;
  justify-content: center;
}

.opcoescor{
  width: 150px;
  height: 150px;
  cursor: pointer;
  border: 3px solid transparent;
  background-size: cover;
  transition: transform 0.2s ease;
}

.opcoescor.selecionada {
  border-color: #3e4042;
}

</style>