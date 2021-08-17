<template>
    <footer class="section">
        <div class="inner clearfix">

            <ul class="site-links float--right">
            <!-- <li><a href="#">Email</a></li>
            <li><a href="#">GitHub</a></li>
            <li><a href="#">Linkedin</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">Blog</a></li> -->
            <!-- <li><a href="#">About</a></li> -->
            <li>© 2021 Peniel Cho, All Rights Reserved.</li>
            </ul>

            <ul class="site-links float--left">
            <!-- <li>© 2021 Peniel Cho, All Rights Reserved.</li> -->
            <!-- <li><a href="#">Terms</a></li>
            <li><a href="#">Privacy</a></li> -->
            <!-- <li><a href="#">Email</a></li>
            <li><a href="#">Linkedin</a></li>
            <li><a href="#">LINE</a></li> -->
            <li><a href="#">Email</a></li>
            <li><a href="#">GitHub</a></li>
            <li><a href="#">Linkedin</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">Blog</a></li>
            </ul>

            <a href="#" class="logo">
            <!-- <svg version="1.0"
                xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                width="24"
                height="24"
                viewBox="0 0 16 16"
                fill="#ccc">
                <path fill-rule="evenodd"
                    d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"></path>
            </svg> -->
            <svg width="100%" height="100%" viewBox="0 0 130 130" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/" style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;">
                <g transform="matrix(4.73424,0,0,4.73424,-145.896,-82.4901)">
                    <text x="31.304px" y="38.437px" style="font-family:'Inter-Regular_Bold', 'Inter', sans-serif;font-size:20.028px;fill:rgb(33,120,255);">P</text>
                    <text x="44.021px" y="38.437px" style="font-family:'Inter-Regular_Bold', 'Inter', sans-serif;font-size:20.028px;">B</text>
                </g>
            </svg>
            </a>

        </div>
    </footer>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.section {
    position: relative;
    /*absolute가 더 못 올라가게 걸릴 수 있도록!*/
}
.section .inner {
    max-width: 1080px;
    margin: 0 auto;
    box-sizing: border-box;
    position: relative;
    /*포지션이 없는 경우에는 부모요소에 position relative 무조건적으로 추가해주기!*/
}
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
footer .inner {
    padding: 50px 0;
    border-top: 1px solid #eee;
}
footer .site-links {
    display: flex;
}
footer .site-links li {
    font-size: 12px;
    margin-right: 10px;
    color: #767676;
    display: inline-block;
}
footer .site-links li a {
    color: #4078c0;
}
footer .site-links li a:hover {
    text-decoration: underline;
}
footer .logo {
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    margin: auto;
    width: 24px;
    height: 24px;
    /*완벽히 가운데 배치 not 정렬!*/
}
footer .logo:hover svg {
    fill: #4078c0;
}

</style>