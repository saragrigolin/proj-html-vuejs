<template>
    <header>
        <div class="container-fluid my_fluid p-0 position-relative">
            <Navbar />
            <div class="jumbo-container">
                <h1 class="m-0 mb-4">Untold Stories</h1>
                <span class="cursive">There is an untold story behind every favorite song.</span>
                <div class="buttons mt-5">
                    <button type="button" class="my_btn btn">latest album</button>
                    <button type="button" class="transparent btn">live dates</button>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
import Navbar from './Navbar.vue';

export default {
    name: "Header",
    components: {
        Navbar,
    },
    methods: {
    },
    created(){
        setTimeout(() => {
            let myNav = document.querySelector('.navbar-container');
            window.onscroll = function() {
            "use strict";
            if (document.body.scrollTop >= 100 || document.documentElement.scrollTop >= 100) {
                myNav.classList.add("scroll");
            } else {
                myNav.classList.remove("scroll");
            }
            };
        }, 300);
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
    
    .jumbo-container {
        text-align: center;
        color: $white;
        padding: 12em 0;
        h1 {
            font-size: 8em;
            font-weight: 700;
        }
        .cursive {
            font-family: $fontFamily;
            font-style: italic;
            font-size: 1.5em;
        }
        .buttons {
            .my_btn, .transparent {
                font-size: 1.5em;
                border-radius: 0.1em;
                padding: 0.7em 2em;
                font-weight: 600;
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