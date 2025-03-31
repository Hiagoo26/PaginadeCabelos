<template>
  <div class="containers">
    <NavBar class="container"></NavBar>
    <div class="content" style="transform: translateY(-480px);">
      <div class="texto">
        <TextoEsquerda class="textoEsq"></TextoEsquerda>
      </div>
      <div class="Slide">
      <SlideBar class="slidebar"></SlideBar>
      </div>
    </div>
    <div class="Menu">
        <SelecionadorMenu class="corcabelo"></SelecionadorMenu>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import SlideBar from './components/SlideBar.vue'
import TextoEsquerda from './components/TextoEsquerda.vue'
import SelecionadorMenu from './components/SelecionadorMenu.vue'



export default {
  name: 'App',
  components: {
    NavBar,
    SlideBar,
    TextoEsquerda,
    SelecionadorMenu
  }
}
</script>

<style>
.containers {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 10px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 20px;
  width: 80%;
  max-width: 1200px;
}

.texto {
  display: flex;
  max-width: 600px;
  text-align: flex-start;
  align-items: center;
  justify-content: center;
  flex: 1;
  min-width: 0;
  word-break: break-word;

}

.Slide{
  flex: 0.2;
  display: flex;
  justify-content: flex-end;
  flex-shrink: 0;

}

.Menu {
  display: flex;
  justify-content: center;
  margin-top: -261px;
  width: 95%;
  max-width: 950px;
  background-color: #9400d3;
  border-radius: 15px;
  box-shadow: 0px 4px 10px #3e4042;

}
</style>
