<template>
    <section>
      <div class="container-descricao container">
        <div class="row d-flex justify-content-center">
          <div class="col-12 col-md-6 d-flex flex-column flex-md-row justify-content-around align-items-center container-dados">
            <div class="descricao">
              <h1>Desempenho</h1>
              <h2>aperfeiçoado</h2>
              <p class="text-sm-center text-lg-start  ">O controle sem fio Xbox traz um design elegante, conforto refinado e compartilhamento instantâneo para um favorito comum.</p>
            </div>
            
            <div>
              <img src="../assets/img/controle-xbox.png" alt="" class="img-fluid controle-xbox">
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ControleComponente'
  }
  </script>
  
  <style lang="scss">
  section {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 6.25rem;
  
    .container-descricao {
      display: flex;
      align-items: center;
      gap: 8.75rem;
      color: white;
      width: 100%;
      max-width: 1216px;  // Ajusta o tamanho máximo do container
  
      .descricao {
        display: flex;
        flex-direction: column;
        gap: 10px;
        text-align: left;
  
        h1, h2 {
          font-size: 4rem;
        }
        
        h1{
            color: var(--bg-btn-secundary);
            
        }
  
        p {
          color: #C0C0C0;
          width: 35.625rem;
        }
      }
  
      .controle-xbox {
        width: 31.25rem;
        height: 18.75rem;
      }
  
      .container-dados {
        display: flex;
        min-width: 76rem;
        height: 23.5625rem;
      }
    }
  }
  
  @media screen and (max-width: 768px) {
    section {
      .container-descricao {
        flex-direction: column;
        gap: 2rem;
        width: 100%;
        
        .descricao {
          text-align: center;
  
          h1, h2 {
            font-size: 1.5rem;
          }

          p{
                width: 100%;
          }
        }
  
        .controle-xbox {
          width: 12.5rem;
          height: 8.9375rem;
        }
  
        .container-dados {
          min-width: 100%;
          height: auto;
        }
      }
    }
  }
  </style>
  