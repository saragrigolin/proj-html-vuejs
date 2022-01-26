<template>
    <footer>
        <!-- footer-top -->
        <div class="footer-top">
            <div class="container-footertop d-flex justify-content-between align-items-center py-5">
                <div class="logo">
                    <img src="../assets/img/logo_footer.png" alt="">
                </div>
                <ul class="d-flex align-items-center m-0 p-0">
                    <!-- creo v-for per i link -->
                    <li v-for="(footerLink, index) in footerLinks" :key="index" class="px-2"><a :href="footerLink.href" :class="(footerLink.isActive) ? 'active' : ''">{{footerLink.name}}</a></li>
                    <!-- <li class="pe-2"><a href="#" class="active">Home</a></li>
                    <li class="px-2"><a href="#">Meet The Brand</a></li>
                    <li class="px-2"><a href="#">Live Dates</a></li>
                    <li class="px-2"><a href="#">Latest News</a></li>
                    <li class="px-2"><a href="#">Albums</a></li>
                    <li class="ps-2"><a href="#">Fans</a></li> -->
                </ul>
            </div>
        </div>
        <!-- /footer-top -->
        <!-- footer-bottom -->
        <div class="footer-bottom">
            <div class="container-footerbottom d-flex justify-content-between align-items-center">
                <!-- copyright -->
                <div class="copyright">
                    <span class="pe-1"><i class="far fa-copyright"></i> Copyright 2021 - 2020</span>
                    <span class="px-1">&vert;</span>
                    <span class="text-uppercase px-1">avada theme by themefusion</span>
                    <span class="px-1">&vert;</span>
                    <span class="text-uppercase px-1">all rights reserved</span>
                    <span class="px-1">&vert;</span>
                    <span class="text-uppercase ps-1">power by wordpress</span>
                </div>
                <ul class="socials d-flex align-items-center m-0 p-0">
                    <!-- creo v-for per i social -->
                    <li v-for="(footerSocial, index) in footerSocials" :key="index" class="px-2">
                        <a :href="footerSocial.href">
                            <i :class="`fab fa-${footerSocial.class}`"></i>
                        </a>
                    </li>
                    <!-- <li class="pe-2"><a href="#"><i class="fab fa-facebook-f"></i></a></li>
                    <li class="px-2"><a href="#"><i class="fab fa-twitter"></i></a></li>
                    <li class="px-2"><a href="#"><i class="fab fa-instagram"></i></a></li>
                    <li class="ps-2"><a href="#"><i class="fab fa-youtube"></i></a></li> -->
                </ul>
            </div>
        </div>
        <button type="button" class="arrow-fixed my_btn btn"><a href="#"><i class="fas fa-chevron-up"></i></a></button>
        <!-- /footer-bottom -->
    </footer>
</template>

<script>
export default {
    name: "Footer",
    data(){
        return {
            footerLinks: [
                {
                    name: 'Home',
                    href: '#',
                    isActive: true,
                },
                {
                    name: 'Meet the brand',
                    href: '#',
                    isActive: false,
                },
                {
                    name: 'Live dates',
                    href: '#livedates',
                    isActive: false,
                },
                {
                    name: 'Latest news',
                    href: '#latestnews',
                    isActive: false,
                },
                {
                    name: 'Albums',
                    href: '#',
                    isActive: false,
                },
                {
                    name: 'Fans',
                    href: '#',
                    isActive: false,
                }
            ],
            footerSocials: [
                {
                    class: 'facebook-f',
                    href: '#',
                },
                {
                    class: 'twitter',
                    href: '#',
                },
                {
                    class: 'instagram',
                    href: '#',
                },
                {
                    class: 'youtube',
                    href: '#',
                },
            ]
        }
    },
    created(){
        setTimeout(() => {
            let myArrow = document.querySelector('.arrow-fixed');
            window.onscroll = function() {
            "use strict";
            if (document.body.scrollTop >= 400 || document.documentElement.scrollTop >= 400) {
                myArrow.classList.add("show");
            } else {
                myArrow.classList.remove("show");
            }
            };
        }, 300);
    }

}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
.footer-top {
    background-color: $backgroundMusicIsLife;
    .container-footertop {
        padding: 0 5em;
        .logo {
            width: 15%;
            img {
                width: 100%;
            }
        }
        a:hover {
            color: $white;
            transition: color 0.3s linear;
        }
    }
}
.footer-top, .footer-bottom {
    ul {
        li {
            list-style-type: none;
            a {
                text-decoration: none;
                color: $text;
                font-size: 0.8em;
                &.active {
                    color: $white;
                }
            }
        }
    }
}
.footer-bottom {
    background-color: $backgroundMain;
    color: $text;
    .container-footerbottom {
        padding: 2.5em 5em;
        span {
            font-size: 0.8em;
        }
        a {
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8em;
            border-radius: 0.1em;
            width: 3em;
            height: 3em;
            background-color: $backgroundMusicIsLife;
            &:hover {
                color: $backgroundMain;
                background-color: $mandy;
                transition: all 0.5s linear;
            }
        }
    }
}
.arrow-fixed {
    display: none !important;
    position: fixed;
    bottom: 0;
    right: 0;
    z-index: 1000;
    margin: 0 2em;
    padding: 0.5em 1em;
    border-radius: 0 !important;
    a {
        color: $text;
        text-decoration: none;
        &:hover {
            color: $backgroundMain;
        }
    }
}
.show {
    display: inline-block !important;
}
</style>