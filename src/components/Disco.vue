<template>
  <div class="album col-sm-6 col-md-4 col-lg-5 mb-2 ml-3 mr-3">
    <img class="img-fluid figure-img" :src="disco.poster" alt="">
    <h5>{{disco.title}}</h5>
    <h8>{{disco.author}}</h8>
  </div>
</template>

<script>
export default {
  name:'Disco',
  props:{
    disco:Object
  }
}
</script>

<style lang="scss" scoped>

  .album{  
    margin: 1%;
    display: flex;
    flex-direction: column;
    padding: 2%;
    box-shadow: 0 5px 5px rgba(0,0,0,.3);
    transition: all .3s;
    &:hover{
    transform: scale(1.05, 1.05);
    filter:brightness(110%);
    box-shadow: 0 15px 15px rgba(0,0,0,.3);
    }
    text-align: center;
    background-color: #2e3a46;
    color: white;
    h8{
      color: #807f7f;
    }
  }
  img{
    margin-bottom: 20px;
  }

  .col-lg-5{
    position: relative;
    min-height: 1px;
    padding-right: 15px;
    padding-left: 15px;
  }

  @media (min-width: 1000px) {
    .col-lg-5 {
        width: 18%;
        float: left;
    }
  } 
</style>