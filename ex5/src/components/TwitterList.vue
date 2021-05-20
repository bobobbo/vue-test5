<template>

    <div>
        TwitterList page
        <br/>
        <ul v-for="(item,idx) in items" :key="idx" :item="item"/>
            <li><router-link to="/detail/{{id}}"><CardView/></router-link></li>
        </ul>
        <!-- <ul>
            <li><router-link to="/detail/1">This is card</router-link></li>
            <li><router-link to="/detail/2">This is card</router-link></li>
            <li><router-link to="/detail/3">This is card</router-link></li>
            <li><router-link to="/detail/4">This is card</router-link></li>
            <li><router-link to="/detail/5">This is card</router-link></li>
            <li><router-link to="/detail/6">This is card</router-link></li>
            <li><router-link to="/detail/7">This is card</router-link></li>
            <li><router-link to="/detail/8">This is card</router-link></li>
            <li><router-link to="/detail/9">This is card</router-link></li>
        </ul> -->
    </div>
</template>
<script>
export default {
    name: 'TwitterList',
    props: {
        msg : String
    },
    data(){
        return {
            items : [
                {
                id : 1,
                image : 'https://source.unsplash.com/random?q=1' ,
                title : '1번째 게시글' ,
                contents : 'contents',
                name : '@kawaidanbi'
            },
            {
                id : 2,
                image : 'https://source.unsplash.com/random?q=2' ,
                title : '2번째 게시글' ,
                contents : 'contents',
                name : '@y._.b'
            },
            {
                id : 3,
                image : 'https://source.unsplash.com/random?q=3' ,
                title : '3번째 게시글' ,
                contents : 'contents',
                name : '@minji0_rose'
            },
            {
                id : 4,
                image : 'https://source.unsplash.com/random?q=4' ,
                title : '4번째 게시글' ,
                contents : 'contents',
                name : '@Kate_9love'
            },
            {
                id : 5,
                image : 'https://source.unsplash.com/random?q=5' ,
                title : '5번째 게시글' ,
                contents : 'contents',
                name : '@minji'
            },
            {
                id : 6,
                image : 'https://source.unsplash.com/random?q=6' ,
                title : '6번째 게시글' ,
                contents : 'contents',
                name : '@Vanilla_Min'
            },
            {
                id : 7,
                image : 'https://source.unsplash.com/random?q=7' ,
                title : '7번째 게시글' ,
                contents : 'contents',
                name : '@Chocolate'
            },
            {
                id : 8,
                image : 'https://source.unsplash.com/random?q=8' ,
                title : '8번째 게시글' ,
                contents : 'contents',
                name : '@Pin_k'
            },
            {
                id : 9,
                image : 'https://source.unsplash.com/random?q=9' ,
                title : '9번째 게시글' ,
                contents : 'contents',
                name : '@168c'
            }
            ]
        }
    }
    
}
</script>
<style scoped>
    ul,li{list-style: none;}
</style>