<template>
    <div class="full">
        <div class="contents">
            <div class="logo">
                <img 
                width="130px"
                lazy-src="../assets/instagram_logo.png"
                src="../assets/instagram_logo.png">
            </div>
            <div class="search">
                <input type="text" value="검색">
            </div>
            <div class="icon">
                <i class="far fa-heart"></i>
            </div>
        </div>
    </div>
</template>
<script>
    export default {}
</script>
<style>
    .full{
        width: 100%;
        height: 60px;
        border-bottom: solid 1px #eee;
    }
    .contents{
        position: relative;
        max-width: 700px;
        margin: 0 auto;
        padding: 10px;
        box-sizing: border-box;
    }
    .logo{
        float: left;
        cursor: pointer;
    }
    .search{
        width: 140px;
        margin: 0 auto;
        margin-top: 5px;
    }
    .icon{
        position: absolute;
        top: 15px;
        right: 0;
        font-size: 20px;
        cursor: pointer;
    }
</style>