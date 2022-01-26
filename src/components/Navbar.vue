<template>
    <div class="navbar-container position-fixed">
        <nav class="navbar navbar-dark px-5">
            <a class="navbar-brand my_navbar-brand" href="#">
                <img src="../assets/img/avada-music-logo.png" alt="">
            </a>
            <button class="navbar-toggler my_navbar-toggler" @click="getCollapse()">
                <span class="navbar-toggler-icon open"></span>
            </button>
            <div class="navbar-collapse my_collapse">
                <button class="navbar-toggler my_navbar-toggler" @click="getCollapse()">
                    <i class="close fas fa-times"></i>
                </button>
                <div class="navbar-nav my_navbar-nav">
                    <a v-for="(navLink, index) in navLinks" :key="index" :href="navLink.href" class="nav-item nav-link" :class="(navLink.isActive) ? 'active' : ''" @click="getCollapse()">{{navLink.name}}</a>
                    <!-- <a class="nav-item nav-link active" href="#">Home</a>
                    <a class="nav-item nav-link" href="#">Meet the brand</a>
                    <a class="nav-item nav-link" href="#">Live dates</a>
                    <a class="nav-item nav-link" href="#">Latest news</a>
                    <a class="nav-item nav-link" href="#">Albums</a>
                    <a class="nav-item nav-link" href="#">Fans</a> -->
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: "Navbar",
    data (){
        return {
            navLinks: [
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
        }
    },
    methods: {
        getCollapse(){
            let collapse = document.querySelector('.my_collapse');
            if(collapse.classList.contains("show")){
                collapse.classList.remove("show");
            } else {
                collapse.classList.add("show");
            }
        }

    }
}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
// navbar
.navbar-container {
    top: 0;
    left: 0;
    width: 100%;
    z-index: 10;
    &.scroll {
        background-color: #1F212B;
    }
    .my_navbar-brand {
        width: 15%;
        img {
            width: 100%;
        }
    }
    .navbar-dark {
        .my_navbar-toggler {
            border: none;
        }
        .my_navbar-toggler:focus {
            box-shadow: none;
        }
        .my_collapse {
            position: absolute;
            text-align: center;
            visibility: hidden;
            opacity: 0;
            height: 100vh;
            width: 100%;
            top: 0;
            left: 0;
            background-color: $mandy;
            transition: all 0.3s linear;
            &.show {
                visibility: visible;
                opacity: 1;
            }
            .my_navbar-toggler {
                position: absolute;
                top: 0;
                right: 0;
                margin: 0.8em 2.5em;
            }
            .my_navbar-nav {
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%,-50%);
            }
            .nav-item {
                font-size: 2em;
                font-weight: 300;
            }
        }
        .close {
            font-size: 1.6em;
        }
    }
}
</style>