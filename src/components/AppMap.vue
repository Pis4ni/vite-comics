<script>
import {buildImgPath} from '../utils/img'
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
    <div class="mapContainer">
      <div class="list" v-for="(element, i) in map">
        <h3>
        {{map[i].listName}}
        </h3>
        <ul>
          <li v-for="(link, index) in map[i].listLinks">
            {{map[i].listLinks[index]}}
          </li>
        </ul>

      </div>
      <img :src="buildImgPath(wathermark)" alt="">
    </div>
</template>

<style lang="scss" scoped>
.mapContainer{
  color: #fffffe;
  background-image:url(../assets/img/footer-bg.jpg) ;
  display: flex;
  flex-direction: column;
  align-content: flex-start;
  flex-wrap: wrap;
  max-height: 400px;
  padding: 1rem;
  position: relative;
  overflow: hidden;
  .list{
    text-transform: uppercase;
    ul{
      list-style: none;
      margin: 0;
      padding: 0;
      li{
        text-transform: capitalize;
      }
    }
  }
  img{
    position:absolute;
    right:100px;
    top: 0;
    transform: translateY(-20%);
  }
}
</style>