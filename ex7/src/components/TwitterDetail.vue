<template>
<div class="flex">
  <div>
    <h3>:) ...</h3>
    <div class="btn-back">
      <div class="btn-back">
        <router-link to="/" tag="button">Back</router-link>
      </div>
    </div>
    <!-- <div class="card-name">{{item.id}}</div> -->
  </div>
</div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'TwitterDetail',
  props: {
    id: String,
    // msg: String
  },
  data(){
    return {
      items:[],
      // data:[]
    }
  },
  mounted(){
    axios.get('https://dummyapi.io/data/api/user/0F8JIqi4zwvb77FGz6Wt', {
      'headers' : {
        "app-id" : '60bdce2088e259cd82ab4802'
      }
    })
        .then((res) => {
          this.items = res.data.data;
          console.log( this.items );
          // this.items = res.data.id;
          // console.log(res);
          // console.log( res.items );
        });
        // .catch((err) => {
        //   console.log(err);
        // })
        // .then(() => {
        // });
  }
}
</script>

<style scoped>
.flex{
   display: flex;
   height: 95vh;
   display: flex;
   justify-content: center;
   align-items: center;
}
button{
  width: 100px;
  height: 25px;
  border-radius: 10px;
  background: linear-gradient(#e83e8c, #ffc107);
  color: white;
  font-weight: bold;
}
</style>