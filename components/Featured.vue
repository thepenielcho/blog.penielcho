<template>
    <div class="container">
        <div class="inner">
            <div class="postpic">
                <nuxt-link to='/first-post'>
                    <img src="../assets/resources/testimg.jpeg" alt="">
                </nuxt-link>
            </div>
            <div class="txtinner">
                <nuxt-link to='/first-post'>
                    <div class="posttitle">My first blog post</div>
                </nuxt-link>
                <div class="postdes">For example you could define an icon for *.sample and every file that ends with .sample will have the defined icon.
                    sample and every file that ends with .sample will have the defined icon. sample and every file that ends with .sample will have the defined icon.
                </div>
                <nuxt-link to='/first-post'>
                    <div class="postdetails">더 알아보기 ></div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .inner {
        max-width: 1080px;
        margin: 0 auto;
        box-sizing: border-box;
        position: relative;
    }
    .postpic {
        width: 1080px;
        height: 462px;
        overflow: hidden;
        border-radius: 15px;
        margin: auto;
    }
    .postpic img {
        width: 1080px;
        height: auto;
    }
    .txtinner {
        margin: 20px 0;
    }
    .posttitle {
        font-size: 30px;
        font-weight: bold;
        color: #000;
        margin-bottom: 19px;
    }
    .postdes {
        font-size: 18px;
        font-weight: 300;
        color: #A4ABB5;
        margin-bottom: 25px;
    }
    .postdetails {
        font-size: 16px;
        font-weight: 300;
        color: #3282F6;
    }
</style>