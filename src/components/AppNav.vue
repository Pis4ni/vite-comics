<script>
  import {buildImgPath} from '../utils/img'
  export default {
    data(){
      return {
        test:'App Nav',
        linkCards:[
          {
          imgName:'buy-comics-digital-comics.png',
          link:'#',
          name:'digital comics'
          },
          {
          imgName:'buy-comics-merchandise.png',
          link:'#',
          name:'DC merchandise'
          },
          {
          imgName:'buy-comics-subscriptions.png',
          link:'#',
          name:'subscription'
          },
          {
          imgName:'buy-comics-shop-locator.png',
          link:'#',
          name:'comic shop locator'
          },
          {
          imgName:'buy-dc-power-visa.svg',
          link:'#',
          name:'dc power visa'
          },
        ],
      }
    },
    methods: {
      buildImgPath
    }
  }
</script>

<template>
    <div>
      <div class="link-card" v-for="(card,index) in linkCards ">
        <div class="miniature">
          <img :src="buildImgPath(linkCards[index].imgName)" alt="">
        </div>
        <span>
          {{ linkCards[index].name }}
        </span>
      </div>
    </div>
</template>

<style lang="scss" scoped>
div{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 0;
  background-color:#0c7cec ;
  .link-card{
    padding: 0 2rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .miniature{
      height: 50px;
      width: 50px;
      img{
        width:100%
      }
    }
    span{
      margin: 0 1rem;
      color:#fafcfd ;
      text-transform: uppercase;
      text-wrap: nowrap;
    }
  }
}
</style>