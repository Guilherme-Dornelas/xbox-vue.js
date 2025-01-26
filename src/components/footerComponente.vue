<template>

<footer>
    <img src="../assets/img/logo-xbox.svg" alt="" class="img-fluid">
    <div class="d-block  d-lg-flex gap-3"> 
        <p>© Microsoft 2022</p>
        <p>Todos os direitos reservados</p>
    </div>
</footer>

</template>
<script>

export default {
    name: 'FooterComponente'
}
</script>

<style>
  footer{
    display: flex;
    justify-content: space-around;
    padding: 1.25rem;
    width: 100%;
    height: auto;
    
    p{
        color: white;
        text-align: left;
        margin-bottom: 0px !important;

    }
  }

  @media screen and (min-width: 992px){
    footer{
        
        p{
            color: white;
            font-size: 0.75rem;
            margin-bottom: 0px !important;

        }

        img{
            width: 5.1875rem;
            height: 1.5rem;
        }


    }
    
  }
</style>