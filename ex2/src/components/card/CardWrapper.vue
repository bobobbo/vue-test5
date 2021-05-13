<template>
  <div class="card-wrapper">
    <Card v-for="(item,idx) in items" :key="idx" :item="item"/>
  </div>
</template>

<script>
import Card from '@/components/card/Card.vue'

export default {
  name: 'CardWrapper',
  components: {
    Card
  },
  data(){
    return {
        items : [
            {
                image : 'https://source.unsplash.com/random?q=1' ,
                title : '1번째 게시글' ,
                contents : 'contents',
                name : '@kawaidanbi'
            },
            {
                image : 'https://source.unsplash.com/random?q=2' ,
                title : '2번째 게시글' ,
                contents : 'contents',
                name : '@y._.b'
            },
            {
                image : 'https://source.unsplash.com/random?q=3' ,
                title : '3번째 게시글' ,
                contents : 'contents',
                name : '@minji0_rose'
            },
            {
                image : 'https://source.unsplash.com/random?q=4' ,
                title : '4번째 게시글' ,
                contents : 'contents',
                name : '@Kate_9love'
            },
            {
                image : 'https://source.unsplash.com/random?q=5' ,
                title : '5번째 게시글' ,
                contents : 'contents',
                name : '@minji'
            },
            {
                image : 'https://source.unsplash.com/random?q=6' ,
                title : '6번째 게시글' ,
                contents : 'contents',
                name : '@Vanilla_Min'
            },
            {
                image : 'https://source.unsplash.com/random?q=7' ,
                title : '7번째 게시글' ,
                contents : 'contents',
                name : '@Chocolate'
            },
            {
                image : 'https://source.unsplash.com/random?q=8' ,
                title : '8번째 게시글' ,
                contents : 'contents',
                name : '@Pin_k'
            },
            {
                image : 'https://source.unsplash.com/random?q=9' ,
                title : '9번째 게시글' ,
                contents : 'contents',
                name : '@168c'
            },
            {
                image : 'https://source.unsplash.com/random?q=10' ,
                title : '10번째 게시글' ,
                contents : 'contents',
                name : '@yerinb'
            }
        ]
    }
  }
}
</script>

<style scoped>
.card-wrapper{
    max-width:500px;
    margin: 0 auto;
}
</style>
