<template>
  <div class="story-wrapper">
    <Story v-for="(item,idx) in items" :key="idx" :item="item"/>
  </div>
</template>

<script>
import Story from '@/components/Story.vue'

export default {
  name: 'StoryWrapper',
  components: {
    Story
  },
  data(){
    return {
        items : [
            {
                image : 'https://source.unsplash.com/random?q=1' ,
            },
            {
                image : 'https://source.unsplash.com/random?q=2' ,
            },
            {
                image : 'https://source.unsplash.com/random?q=3' ,
            },
            {
                image : 'https://source.unsplash.com/random?q=4' ,
            },
            {
                image : 'https://source.unsplash.com/random?q=5' ,
            },
            {
                image : 'https://source.unsplash.com/random?q=5' ,
            }
        ]
    }
  }
}
</script>

<style scoped>
.story-wrapper{
    max-width:500px;
    height: 100px;
    margin: 0 auto;
    padding: 19px;
}
</style>
