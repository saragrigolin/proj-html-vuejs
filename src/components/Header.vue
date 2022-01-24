<template>
    <header>
        <div class="container-fluid p-0">
            <div class="navbar-container">
                <nav class="navbar navbar-dark px-3">
                    <a class="navbar-brand my_navbar-brand" href="#">
                        <img src="../assets/img/avada-music-logo.png" alt="">
                    </a>
                    <button class="navbar-toggler my_navbar-toggler" @click="getBackground()" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon open"></span>
                        <i class="close fas fa-times"></i>
                    </button>
                    <div class="collapse navbar-collapse my_collapse" id="navbarNavAltMarkup">
                        <div class="navbar-nav">
                        <a class="nav-item nav-link active" href="#">Home</a>
                        <a class="nav-item nav-link" href="#">Meet the brand</a>
                        <a class="nav-item nav-link" href="#">Live dates</a>
                        <a class="nav-item nav-link" href="#">Latest news</a>
                        <a class="nav-item nav-link" href="#">Albums</a>
                        <a class="nav-item nav-link" href="#">Fans</a>
                        </div>
                    </div>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
// import "bootstrap";
export default {
    name: "Header",
    methods: {
        getBackground(){
            let myNavbar = document.querySelector('.navbar');
            let ariaExpanded = document.querySelector(".my_navbar-toggler").getAttribute("aria-expanded");
            if(ariaExpanded == "true"){
                myNavbar.classList.add('red');
            }else {
                myNavbar.classList.remove('red');
            }
        }
    }

}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";

.container-fluid {
    background-image: url('../assets/img/home_slider.jpg');
    background-size: cover;
    background-position: 50%;
    height: 600px;
    .my_navbar-brand {
        width: 15%;
        img {
            width: 100%;
        }
    }
    .my_navbar-toggler {
        border: none;
    }
    .my_navbar-toggler:focus {
        box-shadow: none;
    }
    .my_collapse {
        text-align: center;
    }
    .close {
        font-size: 1.6em;
    }
    button[aria-expanded="true"] > span.navbar-toggler-icon {
        display: none;
    }

    button[aria-expanded="false"] > .close {
        display: none;
    }
    .navbar.red {
        background-color: $mandy;
    }
    .navbar-dark {
        transition: background-color 150ms linear;
    }
}
</style>