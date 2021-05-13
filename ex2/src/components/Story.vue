<template>
  <div class="story">
    <img :src="item.image" alt="Card image cap">
  </div>
</template>

<script>
export default {
  name: 'Story',
  props: {
    item: Object
  }
}
</script>

<style scoped>
.story{
    width: 70px;
    height: 70px;
    border-radius: 200px;
    display: inline-block;
    margin-right: 7px;
    cursor: pointer;
}
.story img{
    width: 100%;
    height: 100%;
    border-radius: 50px;
}
</style>
