<template>
  <header>
    <nav>
      <div class="menu-toggle" @click="toggleMenu">&#9776;</div>
      <ul :class="{ show: isMenuOpen }">
        <li><a href="#home" @click="toggleMenu">Home</a></li>
        <li><a href="#Tipos_de_Golpes" @click="toggleMenu">Tipos de Golpes</a></li>
        <li><a href="#Dicas_de_Seguranca" @click="toggleMenu">Dicas de Segurança</a></li>
        <li><a href="#O_que_Fazer_se_For_Vítima" @click="toggleMenu">O que Fazer se For Vítima ?</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<style>
header {
  background: #108fca;
  color: rgb(245, 240, 240);
  padding: 1rem 0;
  position: fixed;
  width: 100%;
  height: 40px;
  top: 0;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  padding: 0;
}

nav ul li {
  margin: 0 1rem;
}

nav ul li a {
  color: rgb(255, 255, 255);
  text-decoration: none;
  font-weight: 700;
}

nav ul li a:hover {
  text-decoration: underline;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    background: #108fca;
    position: absolute;
    width: 100%;
    top: 40px;
    left: 0;
    display: none;
  }
  
  nav ul li {
    margin: 1rem 0;
  }

  nav ul.show {
    display: flex;
  }
}

nav .menu-toggle {
  display: none;
}

@media (max-width: 768px) {
  nav .menu-toggle {
    display: block;
    position: absolute;
    top: 15px;
    right: 15px;
    font-size: 1.5rem;
    cursor: pointer;
  }
}
</style>
