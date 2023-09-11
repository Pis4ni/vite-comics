<script>
  export default {
    data(){
      return {
        test:'card'
      }
    },
    props:['thumb', 'price', 'series', 'type',]

  }
</script>

<template>
    <div class="card-comic mb-4">
        <div class="img-thumb">
            <img :src="thumb" alt="">
        </div>
        <span>
            {{ series }}
        </span>
    </div>
</template>

<style lang="scss" scoped>
.card-comic{
    width: calc((100% - 6rem)/6);
    display: flex;
    flex-direction: column;
    .img-thumb{
        border: 1px solid black inset;
        border-radius: .5rem;
        height: 225px;
        overflow: hidden;
        
        img{
            max-width: 100%;
        }
    }
    span{
        color: #ffffff;
        margin: 1rem 0;
        text-transform: uppercase;
    }
}
    
</style>