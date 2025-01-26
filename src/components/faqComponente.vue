<template>
    <section class="container-faq">
      <div class="teste">
        <!-- Item 1 -->
        <div class="accordion-item">
          <div class="accordion-header" @click="toggleAccordion(1)">
            <h2>Meus jogos anteriores do Xbox vão funcionar no Xbox Series X?</h2>
            <i :class="{'bi bi-chevron-up  Up': activeIndex === 1, 'bi bi-chevron-down': activeIndex !== 1}"></i>
          </div>
          <div class="accordion-body" v-show="activeIndex === 1">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
          </div>
        </div>
  
        <!-- Item 2 -->
        <div class="accordion-item">
          <div class="accordion-header" @click="toggleAccordion(2)">
            <h2>O que está incluído no Xbox Series X?</h2>
            <i :class="{'bi bi-chevron-up  Up': activeIndex === 2, 'bi bi-chevron-down': activeIndex !== 2}"></i>
          </div>
          <div class="accordion-body" v-show="activeIndex === 2">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
          </div>
        </div>
  
        <!-- Item 3 -->
        <div class="accordion-item">
          <div class="accordion-header" @click="toggleAccordion(3)">
            <h2>Como sei se minha TV é compatível com 4K?</h2>
            <i :class="{'bi bi-chevron-up  Up': activeIndex === 3, 'bi bi-chevron-down': activeIndex !== 3}"></i>
          </div>
          <div class="accordion-body" v-show="activeIndex === 3">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        activeIndex: null, // Índice do acordeão aberto
      };
    },
    methods: {
      toggleAccordion(index) {
        // Alterna entre abrir/fechar o acordeão
        this.activeIndex = this.activeIndex === index ? null : index;
      },
    },
  };
  </script>
  
  <style scoped>
  .container-faq {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  
  .teste {
    color: #fff;
    border-radius: 0.5rem;
    padding: 0.625rem;;
    width: 76rem;
  }
  
  /* Estilo de cada item do acordeão */
  .accordion-item {
    border-bottom: 0.0625rem solid #2e2e2e;
    margin-bottom: 0.625rem;
    padding-bottom: 0.625rem;
  }
  
  /* Cabeçalho do acordeão */
  .accordion-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
    padding: 0.625rem;
    font-size: 1rem;
    border-radius: 0.3125rem;
    transition: background-color 1s;
  
    h2 {
      font-size: 1rem;
    }
  }
  
  /* Corpo do acordeão */
  .accordion-body {
    padding: 0.625rem;
    border-radius: 0.3125rem;
    margin-top: 0.3125rem;

    p {
      color: #ddd;
      text-align: left;
    }
  }
  
  .Up {
    color: var(--bg-btn-secundary);
  }

  @media screen and (max-width: 768px) {
    .teste {
      width: 100%;

       /* Cabeçalho do acordeão */
        .accordion-header {
            display: flex;
            align-items: center;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 0.3125rem;
            transition: background-color 1s;
        
            h2 {
                font-size: 1rem;
                text-align: left;
                width: 16.4375rem;
            }
  }
    }
    
  }
  </style>