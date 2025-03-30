<template>
    <div class="container">
        <nav class="navbar">
          <div class="navbarcontent">
              <img class="logo" src="@/assets/logo_final.png" alt="logo">
          </div>
      </nav>
    </div>
</template>


<style scoped>
.container {
  margin-top: 60px;
  font-size: 52px;
  margin: 15%;
  justify-content: center;
  justify-items: center;

}

.navbar {
  background: linear-gradient(135deg, #9400d3, #3e4042);
  height: 100px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  padding: 10px;
}

.navbarcontent {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 20px;
}

.logo {
  max-width: auto;
  height: 100px;
}
</style>