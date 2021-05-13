<template>
  <div id="app">
    <Header/>
    <StoryWrapper/>
    <CardWrapper/>
  </div>
</template>

<script>
import CardWrapper from '@/components/card/CardWrapper.vue';
import Header from "@/components/Header.vue";
import StoryWrapper from "@/components/StoryWrapper.vue";

export default {
  name: 'App',
  components: {
    CardWrapper,
    Header,
    StoryWrapper
  }
}
</script>

<style>
</style>
