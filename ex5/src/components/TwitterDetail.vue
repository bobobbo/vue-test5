<template>
    <div>
        <div class="btn-back">
            <router-link to="/" tag="button">back</router-link>
        </div>
        Twitter Detail Page with{{id}}
    </div>
</template>
<script>
import axios from 'axios';

export default {
    name : 'TwitterDetail',
    props: {
        id: String
    },
    data(){
        return {
            "appId": "609d61a3cfa64e21a68b8e5c"
        }
    },
    mounted(){
    // ajax with axios
    axios.get('https://dummyapi.io/data/api/user?limit=10' , {
      'headers' : {
        "app-id" : this.appId
      }
    })
    .then((res) => {
      console.log( res.data );
    });
  }
}
</script>
<style scoped>
</style>
