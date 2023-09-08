<script>
  export default {
    data(){
      return {
        test:'~~--> Content goes here <--~~'
      }
    }
  }
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <h2>
        {{ test }}            
      </h2>
    </div>

  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  background-color:#1c1c1c;
  div{
    height: 100%;
    padding: 2rem 0;
    h2{
      color:#f5fbfe;
      margin: 0%;
      font-size:2rem;
    }
  }
}
</style>