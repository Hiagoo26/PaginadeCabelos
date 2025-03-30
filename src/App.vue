<template>
  <div class="container">
    <NavBar class="container"></NavBar>
    <div class="content">
      <div class="text">
        <TextoEsquerda class="textoEsq"></TextoEsquerda>
      </div>
      <div class="containerslide">
      <SlideBar class="slidebar"></SlideBar>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import SlideBar from './components/SlideBar.vue'
import TextoEsquerda from './components/TextoEsquerda.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    SlideBar,
    TextoEsquerda
  }
}
</script>

<style>
.container {
  flex: 1;
  flex-direction: column;
  margin-top: 20px;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  padding: 20px;

}

.text {
  display: flex;
  max-width: 600px;
  text-align: flex-start;
  align-items: center;
  justify-content: center;

}

.containerslide {
  flex: 0.2;
  display: flex;
  justify-content: flex-end;

}
</style>
