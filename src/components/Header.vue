<template>
    <header>
        <div class="container-fluid my_fluid p-0 position-relative">
            <div class="navbar-container position-fixed">
                <nav class="navbar navbar-dark px-3">
                    <a class="navbar-brand my_navbar-brand" href="#">
                        <img src="../assets/img/avada-music-logo.png" alt="">
                    </a>
                    <button class="navbar-toggler my_navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon open"></span>
                        <i class="close fas fa-times"></i>
                    </button>
                    <div class="collapse navbar-collapse my_collapse" id="navbarNavAltMarkup">
                        <button class="navbar-toggler my_navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                            <i class="close fas fa-times"></i>
                        </button>
                        <div class="navbar-nav my_navbar-nav">
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
            <div class="jumbo-container">
                <h1 class="m-0 mb-4">Untold Stories</h1>
                <span class="cursive">There is an untold story behind every favorite song.</span>
                <div class="buttons mt-5">
                    <button type="button" class="btn my_btn">latest album</button>
                    <button type="button" class="btn my_btn transparent">live dates</button>
                </div>
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

.my_fluid {
    background-image: url('../assets/img/home_slider.jpg');
    background-size: cover;
    background-position: 50%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    .navbar-container {
        top: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        .my_navbar-brand {
            width: 15%;
            img {
                width: 100%;
            }
        }
        .navbar.red {
            background-color: $mandy;
        }
        .navbar-dark {
            transition: background-color 700ms ease;
            position: relative;
            .my_navbar-toggler {
                border: none;
            }
            .my_navbar-toggler:focus {
                box-shadow: none;
            }
            .my_collapse {
                position: absolute;
                text-align: center;
                height: 100vh;
                width: 100%;
                top: 0;
                left: 0;
                background-color: $mandy;
                .my_navbar-toggler {
                    position: absolute;
                    top: 0;
                    right: 0;
                    margin: 1.1em;
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
            .collapsing {
                transition: none;
            }
            .close {
                font-size: 1.6em;
            }
            // button[aria-expanded="true"] > span.navbar-toggler-icon {
            //     display: none;
            // }

            button[aria-expanded="false"] > .close {
                display: none;
            }
        }
    }
    .jumbo-container {
        text-align: center;
        color: $white;
        padding: 12em 0;
        h1 {
            font-size: 8em;
            font-weight: 700;
        }
        .cursive {
            font-family: $cursive;
            font-size: 1.5em;
        }
        .buttons {
            .my_btn {
                text-transform: uppercase;
                background-color: $mandy;
                color: $white;
                font-size: 1.5em;
                border-radius: 0.1em;
                padding: 0.7em 2em;
                font-weight: 600;
            }
            .my_btn:hover {
                background-color: $white;
                color: $charade;
            }
            .transparent {
                background-color: transparent;
                border: 1px solid $white;
                margin-left: 2em;
            }
        }
    }
}
</style>