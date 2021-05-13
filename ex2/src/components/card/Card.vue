<template>
  <div class="card text-center">
    <div class="card-proflie">
        <img class="card-circle" :src="item.image">
      <div class="card-name">{{item.name}}</div>
      <div class="card-right" @click="popUp"><i class="fas fa-ellipsis-h"></i></div>
    </div>
    <img class="card-img-top" :src="item.image" alt="Card image cap">
    <div class="card-body">
        <h5 class="card-title">{{item.title}}</h5>
        <p class="card-text">{{item.contents}}</p>
        <a href="#" class="btn btn-primary" @click="viewDetail">View Detail</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    item: Object
  },
  methods : {
      viewDetail(){
          alert('View Detail!!!');
      },
      popUp(){
        alert('팝업창을 띄우고 싶었는데ㅔ!!!!!!ㅠㅠㅠ');
      }
  }
}
</script>

<style scoped>
.card{
    margin:10px;
}
.card-title{
  font-size: 20px;
  font-weight: bold;
}
.card-proflie{
  padding: 10px;
  border-bottom: solid 1px #eee;
}
.card-circle{
  width: 40px;
  height: 40px;
  background-color: black;
  border-radius: 50px;
  float: left;
}
.card-circle img{
  width: 100%;
  height: 100%;
}
.card-name{
  float: left;
  line-height: 35px;
  margin-left: 10px;
  cursor: pointer;
}
.card-name:hover{
  text-decoration: underline;
}
.card-right{
  float: right;
  line-height: 35px;
  cursor: pointer;
  color: black;
}
</style>
