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
    <div>
        <p>
            {{ test }}            
        </p>
    </div>
</template>

<style lang="scss" scoped>
div{
  height: 100%;
  background-color:#1c1c1c;
  padding: 1rem;
  p{
    color:#f5fbfe;
    margin: 0%;
  }
}
</style>