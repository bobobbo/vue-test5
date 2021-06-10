<template>
  <div id="full">
     <ListTitle/>
     <div id="wrap">
        <div class="flexBox" v-for="(item,idx) in items" :key="idx">
        <div class="img">
          <img v-bind:src="item.picture">
        </div>
          <div class="user-id">{{item.id}}</div>
          <div class="name">{{item.firstName}}</div>
          <div class="email">{{item.email}}</div>
          <hr>
          <div class="more"><router-link to="/detail/:id">Get Full Profile</router-link></div>
        </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import ListTitle from "@/components/ListTitle.vue";

export default {
  name: 'TwitterList',
  components: {  
     ListTitle, 
   },
  props: {
    msg: String
  },
  data(){
    return {
      items:[

      ]
    }
  },
  mounted(){
    axios.get('https://dummyapi.io/data/api/user?limit=10' , {
      'headers' : {
        "app-id" : '60bdce2088e259cd82ab4802'
      }
    })
    .then((res) => {
      this.items = res.data.data;
      console.log( this.items );
    });
  }
}
</script>

<style scoped>
#full{
  background: linear-gradient(#e83e8c, #ffc107);
}
#wrap{display: flex; background: linear-gradient(#e83e8c, #ffc107); width: 1000px; height: 90vh; margin: 0 auto; flex-direction: row; flex-wrap: wrap; justify-content: space-around; align-items: center;}
.flexBox{
  background-color: white; width: 180px; height: 270px; border-radius: 5px; padding: 10px; box-sizing: border-box;
}
.img{
  width: 130px; height: 130px; margin: 0 auto; margin-bottom: 10px;
}
.img img{
  width: 100%; height: 100%;
}
.user-id{
  font-size: 13px;
  color: #6c757d;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-bottom: 10px;
}
.name{
  font-size: 16px;
  color: #212529;
  font-weight: bold;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-bottom: 2px;
}
.email{
  font-size: 13px;
  color: #6c757d;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
hr{
  margin-bottom: 14px;
}
.more{
  font-size: 13px;
  color: #ae4ba8;  
  margin-bottom: 50px;}

</style>
