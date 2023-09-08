<script>
  import {buildImgPath} from '../utils/img'
  export default {
    data(){
      return {
        test:'test',
        logoImg:'dc-logo.png',
        links:[
          {
          name:'characters',
          link:'#'
          },
          {
          name:'comics',
          link:'#'
          },
          {
          name:'movie',
          link:'#'
          },
          {
          name:'tv',
          link:'#'
          },
          {
          name:'games',
          link:'#'
          },
          {
          name:'collectibles',
          link:'#'
          },
          {
          name:'videos',
          link:'#'
          },
          {
          name:'fans',
          link:'#'
          },
          {
          name:'news',
          link:'#'
          },
          {
          name:'shop',
          link:'#'
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
    <div class="header-container">
      <img :src="buildImgPath(logoImg)" alt="">
      <nav>
        <ul>
          <li v-for="(link, index) in links" >
            <a :href="links[index].link">{{ links[index].name }}</a>
          </li>
        </ul>
      </nav>
    </div>
</template>

<style lang="scss" scoped>
.header-container{
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 130px;
  img{
    margin: 1rem;
  }
  nav{
    height: 100%;
    display: flex;
    ul{
      list-style: none;
      display: flex;
      margin: 0;
      padding: 0;
      li{
        display: flex;
        align-items: center;
        margin: 0 1rem;
        &:hover{
          box-shadow: inset 0px -15px 0px -10px #0c7cec;
        }
        a{
          text-decoration: none;
          color: #343434;
          text-transform: uppercase;
        }
      }
    }
  }
}
</style>