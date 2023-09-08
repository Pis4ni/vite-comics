<!-- AppFooter -->
<script>
  import {buildImgPath} from '../utils/img'
  export default {
    data(){
      return {
        test:'App Footer',
      }
    },
    methods: {
      buildImgPath
    }
  }
</script>

<template>
    <div>
        <p>
            hi, i'm a Footer {{ test }}            
        </p>
    </div>
</template>

<style lang="scss" scoped>

</style>