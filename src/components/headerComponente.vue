<template>
    <header id="headerComponente"  :class="{ sticky: isSticky }">
      <nav>
        <div class="box-logo">
          <img src="../assets/img/logo-xbox.svg" alt="logo">
          <button class="btn-visao">Visão geral</button>
        </div>
        
        <!-- Botão de menu mobile -->
        <button class="menu-toggle" @click="toggleMenu">
          <span :class="{ open: menuAberto }"></span>
          <span :class="{ open: menuAberto }"></span>
          <span :class="{ open: menuAberto }"></span>
        </button>
  
        <!-- Menu -->
        <ul :class="{ 'menu-mobile': true, 'ativo': menuAberto }">
          <li @click="fecharMenu">JOGOS</li>
          <li @click="fecharMenu">GALERIA</li>
          <li @click="fecharMenu">UNBOX</li>
        </ul>
      </nav>
      
      <button class="btn-disponibilidade">VER DISPONIBILIDADE</button>
    </header>
  </template>
  
  <script>
  export default {
    name: 'HeaderComponente',
    data() {
      return {
        menuAberto: false,
        isSticky: false 
      };
    },
    methods: {
      toggleMenu() {
        this.menuAberto = !this.menuAberto;
      },
      fecharMenu() {
        this.menuAberto = false;
      },

      handleScroll() {
    
      this.isSticky = window.scrollY > 0;
      },
    },
    mounted() {
      
      window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() {
    
      window.removeEventListener('scroll', this.handleScroll);
    },
  };
  </script>
  

<style>
header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: auto;
  padding: 1.5rem;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  transition: 0.5s;
}

nav {
  display: flex;
  align-items: center;
  justify-content: space-around;
  width: 37.3125rem;
  color: white;
}

.box-logo {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.btn-visao {
  padding: 0.375rem 0.625rem;
  border-radius: 3.125rem;
  width: 7.1875rem;
  border: none;
  background-color: var(--bg-btn);
  color: white;
  text-align: center;
}

ul {
  display: flex;
  gap: 1.875rem;
}

.btn-disponibilidade {
  height: 2.4375rem;
  padding: 0.75rem 2rem;
  background-color: var(--bg-btn-secundary);
  color: black;
  border: none;
  font-size: 0.75rem;
  font-weight: 700;
}


.menu-toggle{
    display: none;
}

.sticky{
  background-color: #121212;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
}


@media screen and (max-width: 768px) {
  nav {
    width: 100%;
    justify-content: space-between;
  }

  ul {
    position: absolute;
    top: 60px;
    right: 0;
    width: 200px;
    height: 100vh;
    flex-direction: column;
    padding: 1rem;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    display: none;
    background: rgba(255, 255, 255, 0.1); 
    backdrop-filter: blur(10px); 
    -webkit-backdrop-filter: blur(10px); 
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, 0.2); 
    transition: opacity 0.5s ease, transform 0.3s ease-in-out;
}


.menu-mobile.ativo {
    display: flex;
    opacity: 1;
    transform: translateX(0);
    margin-top: 1.5625rem;
}
  .box-logo{
    width: 100%;
    justify-content: space-around;

    img{
        margin-left: -1rem
    };
}


  .menu-toggle {
    display: flex;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
    cursor: pointer;
  }

  .menu-toggle span {
    width: 30px;
    height: 4px;
    background: white;
    transition: 0.3s;
  }

  .menu-toggle span.open:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
  }

  .menu-toggle span.open:nth-child(2) {
    opacity: 0;
  }

  .menu-toggle span.open:nth-child(3) {
    transform: rotate(-45deg) translate(5px, -5px);
  }

  .btn-disponibilidade{
    display: none;
  }
}



</style>