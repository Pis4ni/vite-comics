<script>
import {buildImgPath} from '../utils/img.js'
  export default {
    data(){
      return {
        test:'App Map',
        backgroundImg:'footer-bg',
        wathermark:'dc-logo-bg.png',
        map:[
          {
            listName: 'dc comics',
            listLinks:[
              'Characters',
              'comics',
              'movies', 
              'TV', 
              'games', 
              'videos', 
              'news'
            ]
          },
          {
            listName: 'shop',
            listLinks:[
              'shop DC',
              'shop DC Collectibles',
            ]
          },
          {
            listName: 'dc',
            listLinks:[
              'terms Of Use',
              'Privacy policy (New)',
              'ad Choices',
              'advertising',
              'jobs',
              'subscriptions',
              'talent Workshops',
              'CPSC Certificates',
              'ratings',
              'shop Help',
              'contact Us',
            ]
          },
          {
            listName: 'sites',
            listLinks:[
              'DC',
              'MAD magazine',
              'DC Kids',
              'DC Universe',
              'DC Power Visa',
            ]
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
    <div class="container g-0">
      <div class="map-container py-4">
        <div class="list" v-for="(element, i) in map">
          <h6>
          {{map[i].listName}}
          </h6>
          <ul class="me-2">
            <li v-for="(link, index) in map[i].listLinks">
              {{map[i].listLinks[index]}}
            </li>
          </ul>
  
        </div>
      </div>
      <img :src="buildImgPath(wathermark)" alt="">
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper{
  background-image:url(../assets/img/footer-bg.jpg) ;
  .container{
    position: relative;
    overflow: hidden;
    .map-container{
      color: #fffffe;
      display: flex;
      flex-direction: column;
      align-content: flex-start;
      flex-wrap: wrap;
      max-height: 400px;
      .list{
        text-transform: uppercase;
  
        ul{
          list-style: none;
          margin: 0;
          padding: 0;
          li{
            text-transform: capitalize;
            color: #999999;
            margin-right: 1rem;
            font-size: .8rem;
            cursor: pointer;
            &:last-child{
              margin-bottom: 1rem;
            }
            &:hover{
              color: #fffffe;
            }
          }
        }
      }
    }
    img{
      position:absolute;
      right:0px;
      top: 0;
      transform: translateY(-20%);
    }
  }
    
  }
</style>