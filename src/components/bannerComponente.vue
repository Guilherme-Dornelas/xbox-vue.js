<template>
    <div class="container-xbox">
       <img src="../assets/img/heading.png" alt="Xbox Series" class="nome-xbox">
       <img src="../assets/img/xbox.png" alt="Console Xbox" class="xbox">
    </div>
 </template>
 
 <script>
 export default {
   name: 'BannerComponente'
 }
 </script>
 
 <style>
 /* Container principal */
 .container-xbox {
     display: flex;
     flex-direction: column;
     align-items: center;
     justify-content: center;
     width: 100%;
     max-width: 1200px;
     margin: 0 auto;
     text-align: center;
 }
 
 /* Ajuste para as imagens */
 .nome-xbox,
 .xbox {
     width: 100%;
     max-width: 50rem; 
     height: auto; 
     object-fit: contain;
 }
 
 /* Ajuste específico para a imagem do console */
 .xbox {
     margin-top: -50px; /* Ajuste para evitar sobreposição */
 }
 
 /* Responsividade */
 @media screen and (max-width: 1024px) {
     .nome-xbox,
     .xbox {
         max-width: 600px;
     }
 }
 
 @media screen and (max-width: 768px) {
     .nome-xbox,
     .xbox {
         max-width: 90%; /* Ocupar a largura disponível sem ultrapassar */
     }
 
     .xbox {
         margin-top: -30px;
     }
 }
 
 @media screen and (max-width: 480px) {
     .nome-xbox,
     .xbox {
         max-width: 100%; /* Ocupar toda a tela */
     }
 
     .xbox {
         margin-top: -20px;
     }
 }
 </style>
 