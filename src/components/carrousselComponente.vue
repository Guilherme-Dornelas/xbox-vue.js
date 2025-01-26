<template>

    <section  class="conainer-swiper">
        <Swiper
        :modules="[Navigation, Pagination]"
        class="mySwiper"
        :slides-per-view="1"
        :autoplay="{ delay: 2500 }"
        :loop="true"
        :navigation="true"
        :space-between="20"

      
    >
      <SwiperSlide v-for="slide in slides" :key="slide.id">
        <img :src="slide.banner" alt="" class="banner">
      </SwiperSlide>

    </Swiper>
    </section>
    
  </template>
  
  <script>
  import { Swiper, SwiperSlide } from "swiper/vue";
  import "swiper/swiper-bundle.css"; // Importa os estilos do Swiper
  import { Navigation, Pagination } from "swiper";
  
  export default {
    data() {
      return {
        slides: [],
      };
    },
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        Navigation,
        Pagination,

      };
    },
    mounted() {
      this.fetchSlides();
    },
    methods: {
      fetchSlides() {
        fetch("http://localhost:8080/api/jogos.json")
        .then(response => response.json())
        .then(data => {
          this.slides = data;
        })
      },
    },
  };
  </script>
  
  <style>
  /* Estilize o Swiper como desejar */
  .conainer-swiper{
       width: 100%;
       height: auto;
       margin-top: 6.25rem;
      .mySwiper {
        width: 37.5rem;
        height: 50rem;
            
        .banner{
                width: 30rem;
                height: 50rem;
                transition: 0.5s;
            }
        }
  }

  @media screen and (max-width: 768px) {
    .conainer-swiper{
        .mySwiper {
            width: 19.5rem;
            height: 32.0625rem;
            .banner{
                width: 100%;
                height: 100%;
                transition: 0.5s;
            }
        }
    }
    
  }
  
  </style>
  