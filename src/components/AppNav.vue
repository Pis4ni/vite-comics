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
  <div class="wrapper">
    <div class="container">
      <div class="link-card" v-for="(card,index) in linkCards ">
        <div class="miniature">
          <img :src="buildImgPath(linkCards[index].imgName)" alt="">
        </div>
        <span>
          {{ linkCards[index].name }}
        </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  background-color:#0c7cec ;
  div{
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 0;
    .link-card{
      width: calc((100% - 5rem) / 5);
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      &:nth-child(4) > div > img{
        height: 35px;
      }
      .miniature{
        width: 20%;
        aspect-ratio: 1;
        margin: 0 1rem 0 0 ;
        
        img{
          width:100%;
          max-height: 40px;
          object-fit: contain;
        }
      }
      span{
        color:#fafcfd ;
        text-transform: uppercase;
        text-wrap: nowrap;
        font-size: .8rem;
      }
    }
  }
}
</style>