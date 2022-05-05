<template>
  <header>
    <img src="../assets/img/dc-logo.png" alt="logo DC">

    <ul>
      <li v-for="(nome, index) in headList" :key="index" :class="nome.lock == false? 'active' : ''">{{nome.cosa}}</li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      headList: [
      {
        cosa: 'characters',
        lock: true
      },
      {
        cosa: 'comics',
        lock: false
      },
      {
        cosa: 'movie',
        lock: true
      },
      {
        cosa: 'tv',
        lock: true
      },
      {
        cosa: 'games',
        lock: true
      },
      {
        cosa: 'collectibles',
        lock: true
      },
      {
        cosa: 'videos',
        lock: true
      },
      {
        cosa: 'fans',
        lock: true
      },
      {
        cosa: 'news',
        lock: true
      },
      {
        cosa: 'shop',
        lock: true
      }
    ]
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/variables.scss";
  @import "../style/generals.scss";

  header{
    height: 100px;
    display: flex;
    justify-content: space-around;
    align-items: center;

    img{
      height: 60px;
    }

    ul{
      display: flex;
      list-style-type: none;
      line-height: 100px;

      li{
        height: 100%;
        margin-left: 20px;
        color: $text-color;
        border-bottom: 5px solid transparent;
        text-transform: uppercase;
      }

      li:hover{
        border-bottom: 5px solid $text-color;
      }
    }
  };
</style>
