<template>
    <div class="inner">
        <div class="ad-banner">
            <a href="http://naver.me/xOC27lWD">
                <img src="../assets/resources/navermembership.png" alt="naver membership ads">
            </a>
        </div>
    </div>
</template>

<style>
    .inner {
        max-width: 1150px;
        margin: 0 auto;
        box-sizing: border-box;
        position: relative;
        /*포지션이 없는 경우에는 부모요소에 position relative 무조건적으로 추가해주기!*/
    }
    .ad-banner {
        width: 1080px;
        height: 105px;
        /* box-sizing: border-box; */
        /* object-fit: contain; */
        margin: auto;
    }
    img {
        width: 1080px;
        height: 105px;
    }
</style>