<template>
    <header class="section">
        <div class="inner clearfix">

            <div class="menu-group float--left">
                <div class="logo">
                    <nuxt-link to="/">
                        <img src="../assets/resources/Logo.png" alt="Logo">                    
                    </nuxt-link>
                </div>
            </div>

            <div class="sign-group float--right toggle">
                <ul class="sub-menu">
                    <li><a href="#">Posts</a></li>
                    <li>
                        <nuxt-link to="/projects" class="alta">Projects</nuxt-link>
                        <!-- <a href="#">Projects</a> -->
                    </li>
                    <li><a href="https://github.com/thepenielcho" target="blank">GitHub</a></li>
                </ul>
            </div>

            <div id="toggle-btn">Header Menu Toggle Button</div>

        </div>
    </header>
</template>

<style scoped>
.clearfix::after{
    content: "";
    clear: both;
    display: block;
}
.float--left {
    float: left;
}
.float--right {
    float: right;
}
.section {
    position: relative;
    border-bottom: solid 0.3px #E5E8EB;
    /*absolute가 더 못 올라가게 걸릴 수 있도록!*/
}
.section .inner {
    max-width: 1150px;
    margin: 0 auto;
    box-sizing: border-box;
    position: relative;
    /*포지션이 없는 경우에는 부모요소에 position relative 무조건적으로 추가해주기!*/
}
header {
    background-color: #ffffff;
}
header .inner {
    height: 70px;
}
header .menu-group {
    display: flex;
    align-items: center;
    height: 100%;
    /*로고와 ul의 수평정렬*/
}
header .logo {
  width: 153.8px;
  height: 40px;
  box-sizing: border-box;
  margin: 0 20px;
}
header .logo img {
    width: 153.8px;
    height: 40px;
}
header .sign-group {
    display: flex;
    height: 100%;
    align-items: center;
}
header .sub-menu {
    order: 0;
    /*order는 기본값이 0이기 때문에 생략이 가능하다.*/
    display: flex;
}
header .sub-menu li a{
    margin-right: 20px;
    padding: 8px;
    display: block;
    font-size: 16px;
    font-weight: 300;
    text-align: center;
    color: #000;
}
header .sub-menu li .alta{
    margin-right: 20px;
    padding: 8px;
    display: block;
    font-size: 16px;
    font-weight: 300;
    text-align: center;
    color: #000;
}
header .sub-menu li a:hover{
    color: #2178FF;
}
header .sub-menu li .alta:hover{
    color: #2178FF;
}
#toggle-btn {
    display: none;
    background: url("../assets/resources/Logo.png");
    width: 18px;
    height: 24px;
    position: absolute;
    top: 16px;
    right: 20px;
    cursor: pointer;
    text-indent: -9999px;
}
</style>