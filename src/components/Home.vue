<template>
    <div>
        <div class="page-content">
            <div class="block-format bg-img">
                <!-- <div class="block-format bg-img block-alignment" :style="{backgroundImage: `url(${bgURL})`}"> -->
                <div class="title-block inner block-alignment">
                    <div class="inner title-in tit-color">
                        <h3 align="center">Welcome to</h3>
                        <h4 align="center">WORK BOX</h4>
                        <p align="center">This site is an example of project<br>built with my own.</p>
                        <div class="btnBox inner block-alignment">
                            <div class="signUpBtn block-alignment">
                                Sign Up
                                <router-link to="/register">
                                    <svg width="180" height="45" viewBox="0 0 180 45"
                                        xmlns="http://www.w3.org/2000/svg">
                                        <rect x='0' y='0' fill='none' width="180" height="45" rx="6"></rect>
                                    </svg>
                                </router-link>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="block-format start-info-container">
                <div class="inner info-in">
                </div>
            </div>

            <div class="info-site-container">
                <div class="inner info-in">

                </div>
            </div>

            <div class="footer">
                <div class="inner nav-in">
                    <div class="copyright block-alignment">
                        <p>Copyright 2019 Alpo. Developed by A.L.I.C.E.</p>
                    </div>
                    <div class="topbar-right block-alignment">
                        <span class="icons-footer-style">
                            <a href="#"><i class="fab fa-telegram-plane"></i></a>
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                            <a href="https://www.instagram.com/lissy___p/"><i class="fab fa-instagram"></i></a>
                            <a href="https://m.vk.com/lissy_p"><i class="fab fa-vk"></i></a>
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    // import bgURL from './assets/background.png'
    export default {
        data() {
            return {
                // bgURL
            }
        }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');

    .tit-color {
        color: rgb(226, 180, 30);
        font-weight: bold;
    }

    h3 {
        font-size: 56px;
    }

    h4 {
        font-size: 76px;
    }

    h1 {
        font-size: 36px;
    }

    .bg-img {
        /* background-color: rgb(29, 3, 41); */
        /* background: linear-gradient(to top left, powderblue, pink); */
        /* background: linear-gradient(to top left, rgb(245, 194, 29), rgb(154, 16, 167));  */
        background: linear-gradient(to top left, rgb(154, 16, 167), rgb(39, 11, 77));
        /* background: linear-gradient(to top left, rgb(154, 16, 167),rgb(39, 11, 77));  */
        height: 630px;
    }

    .title-block {
        padding-top: 90px;
    }

    .title-in {
        max-width: 1120px;
        height: auto;
    }

    .info-in {
        max-width: 1120px;
    }

    .start-info-container {
        background-color: rgba(212, 194, 154, 0.959);
        height: 500px;
    }

    .info-site-container {
        background-color: rgb(43, 42, 40);
        height: 300px;
    }

    .footer {
        background-color: rgb(34, 33, 31);
        height: 70px;
    }

    .copyright {
        height: inherit;
        float: left;
        font-size: 12px;
        color: rgba(212, 194, 154, 0.959);
    }

    .icons-footer-style i {
        font-size: 18px;
        margin-left: 9px;
    }

    .btnBox {
        height: 100px;
    }

    .signUpBtn {
        text-transform: uppercase;
        width: 180px;
        height: 45px;
        position: relative;
        font-size: large;
        font-weight: 900;
    }

    svg {
        position: absolute;
        top: 0;
        left: 0;
    }

    svg rect {
        stroke: rgb(226, 180, 30);
        stroke-width: 3;
        transition: 0.7s;
        stroke-dasharray: 400, 0;
    }

    .signUpBtn:hover svg rect {
        stroke-width: 6;
        stroke-dasharray: 115, 107;
        stroke-dashoffset: 40;
    }

    /*--------------------------------------------------------*/
</style>