<!-- AppFooter -->
<script>
  import {buildImgPath} from '../utils/img.js'
  export default {
    data(){
      return {
        test:'App Footer',
        linkIcons:[
          {
          imgName:'footer-facebook.png',
          link:'#',
          name:'facebook'
          },
          {
          imgName:'footer-twitter.png',
          link:'#',
          name:'twitter'
          },
          {
          imgName:'footer-youtube.png',
          link:'#',
          name:'youtube'
          },
          {
          imgName:'footer-pinterest.png',
          link:'#',
          name:'pinterest'
          },
          {
          imgName:'footer-periscope.png',
          link:'#',
          name:'periscope'
          },
        ]
      }
    },
    methods: {
      buildImgPath
    }
  }
</script>

<template>
  <div class="wrapper">
    <div class="container d-flex justify-content-between align-items-center footer-container">
      <div>
        <button class="sign-up-btn">
          sign up now!
        </button>
      </div>
      <div class="d-flex justyfy-content-center align-items-center">
        <h4 class="text-uppercase m-0">
          follow us
        </h4>
        <ul class="d-flex m-0 p-0">
          <li v-for="element in linkIcons" class="m-1">
            <img :src="buildImgPath(element.imgName)" alt="{{ element.name }}">
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  background-color: #303030;
  .footer-container{
    height: 99px;
    h4{
      color: #0c7cec;
    }
    ul{
      list-style: none;
      li{
        cursor: pointer;
      }
    }
    .sign-up-btn{
      border: #0c7cec 2px solid;
      background-color: transparent;
      color: #ffffff;
      text-transform: uppercase;
      padding: .25rem .5rem ;
    }
  }
}
</style>