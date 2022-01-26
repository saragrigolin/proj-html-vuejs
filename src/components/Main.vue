<template>
    <main>
        <!-- sezione music -->
        <div class="main-container music py-5">
            <div class="main-content d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Music Is Life</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
                </div>
            </div>
        </div>
        <!-- /sezione music -->
        <!-- sezione latest news -->
        <div class="main-container pt-5" id="latestnews">
            <div class="main-content d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Latest Band News</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
                </div>
            </div>
            <div class="news-container container py-5">
                <div class="row m-0">
                    <div class="col-8 p-0">
                        <div class="row m-0">
                            <div class="col-12 p-3">
                                <div class="card-1 position-relative" @mouseover="getHover(0)" @mouseleave="removeHover(0)">
                                    <div class="container-text active-text d-flex flex-column p-4">
                                        <span class="card-title">Technology and music</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                    <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                        <span>Technology and music</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-6 p-3">
                                <div class="card-2" @mouseover="getHover(1)" @mouseleave="removeHover(1)">
                                    <div class="container-text active-text d-flex flex-column p-4">
                                        <span class="card-title">While my guitar gently weep</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                    <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                        <span>While my guitar gently weep</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-6 p-3">
                                <div class="card-3" @mouseover="getHover(2)" @mouseleave="removeHover(2)">
                                    <div class="container-text active-text d-flex flex-column p-4">
                                        <span class="card-title">It just sounds better</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                    <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                        <span>It just sounds better</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-12 p-3">
                                <div class="card-4" @mouseover="getHover(3)" @mouseleave="removeHover(3)">
                                    <div class="container-text active-text d-flex flex-column p-4">
                                        <span class="card-title">The flavor of rock</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                    <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                        <span>The flavor of rock</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-4 p-3">
                        <div class="card-5" @mouseover="getHover(4)" @mouseleave="removeHover(4)">
                            <div class="container-text active-text d-flex flex-column p-4">
                                <span class="card-title">Taking it back to the old school</span>
                                <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                            </div>
                            <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                <span>Taking it back to the old school</span>
                            </div>
                        </div>
                        <div class="card-6" @mouseover="getHover(5)" @mouseleave="removeHover(5)">
                            <div class="container-text active-text d-flex flex-column p-4">
                                <span class="card-title">Sharing the stage with a legend</span>
                                <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                            </div>
                            <div class="hover position-absolute not-active d-flex justify-content-center align-items-center">
                                <span>Sharing the stage with a legend</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <button class="all-news btn my_btn py-5">
                <span>view all latest news</span>
            </button>
        </div>
        <!-- /sezione latest news -->
        <!-- sezione video -->
        <div class="video-container py-5 d-flex justify-content-center">
            <div class="video-content w-30">
                <p>“I just listened to it and said to myself, “Man, I really love this album.” Still, today, it just sounds so fresh. It sounds full of ideas. These guys knew what they were doing. They’re good. And they’re inventive. I haven’t heard anything this year that’s as inventive. I don’t really expect to.”</p>
                <img src="../assets/img/band_interview_play_icon.png" alt="" class="mt-4" @click="getVideo()">
            </div>
            <div class="youtube-container not-active position-fixed justify-content-center align-items-center">
                <button class="my_btn btn" @click="getVideo()">chiudi</button>
                <div class="frame">
                    <iframe width="1000" height="600"
                    src="https://www.youtube.com/embed/PBfP8Ltelu4">
                    </iframe>
                </div>
            </div>
        </div>
        <!-- /sezione video -->
        <!-- sezione live dates -->
        <div class="main-container pt-5" id="livedates">
            <div class="main-content d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Live Dates</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
                </div>
            </div>
            <div class="container p-5">
                <LiveDates />
            </div>
            <button class="all-news btn my_btn py-5">
                <span>view all live dates</span>
            </button>
        </div>
        <!-- /sezione live dates -->

    </main>
</template>

<script>
import LiveDates from './LiveDates.vue';
export default {
    name: "Main",
    components: {
        LiveDates,
    },
    methods: {
        removeHover(index){
            let hover = document.querySelectorAll('.hover');
            let text = document.querySelectorAll('.container-text');
            if (hover[index].classList.contains('active')){
                hover[index].classList.remove('active');
                hover[index].classList.add('not-active');
                text[index].classList.add('active-text');
                text[index].classList.remove('not-active-text');
            }
        },
        getHover(index){
            let hover = document.querySelectorAll('.hover');
            let text = document.querySelectorAll('.container-text');
            if (hover[index].classList.contains('not-active')){
                hover[index].classList.remove('not-active');
                hover[index].classList.add('active');
                text[index].classList.remove('active-text');
                text[index].classList.add('not-active-text');
            }
        },
        getVideo(){
            let youtubeContainer = document.querySelector('.youtube-container');
            if (youtubeContainer.classList.contains('not-active')){
                youtubeContainer.classList.remove('not-active');
                youtubeContainer.classList.add('active');
            } else {
                console.log(youtubeContainer);
                youtubeContainer.classList.add('not-active');
                youtubeContainer.classList.remove('active');
            }
        }
    }

}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
    // main container
    .main-container {
        background-color: $backgroundMain;
        color: $white;
        position: relative;
        .main-content {
            margin: 0 auto;
            text-align: center;
            .title-container .title {
                font-weight: 700;
                font-size: 3em;
            }
            .subtitle-container::before {
                content: '';
                width: 150px;
                height: 1px;
                background-color: $text;
                display: block;
                position: absolute;
                top: 0;
                left: 50%;
                transform: translateX(-50%);

            }
            .subtitle-container {
                position: relative;
                .subtitle {
                color: $text;
                font-size: 1em;
            }
            }
        }
        .news-container {
            div[class*="card"] {
                background-size: cover;
                background-position: center;
                position: relative;
                overflow: hidden;
                img {
                    width: 100%;
                }
                .container-text {
                    background-color: $backgroundMusicIsLife;
                    width: 100%;
                    position: absolute;
                    transition: all 0.3s linear;
                    .card-title {
                        color: $mandy;
                        font-weight: 600;
                    }
                    .card-subtitle {
                        color: $text;
                    }
                }
                .active-text {
                        bottom: 0;
                    }
                .not-active-text {
                    bottom: -100%;
                }
                .hover {
                    height: 100%;
                    width: 100%;
                    top: 0;
                    background-color: $mandy;
                    opacity: 0.8;
                    transition: all 0.3s linear;
                    font-size: 1.6em;
                }
                .not-active {
                    left: -100%;

                }
                .active {
                    left: 0;
                }
            }
            .card-1 {
                background-image: url('../assets/img/blog_music_techo-800x400.jpg');
            }
            .card-2 {
                background-image: url('../assets/img/blog-post3-600x900.jpg');
            }
            .card-3 {
                background-image: url('../assets/img/blog-post4-400x600.jpg');
            }
            .card-4 {
                background-image: url('../assets/img/blog_flavor_rock-800x400.jpg');
            }
            .card-5 {
                background-image: url('../assets/img/blog-post1-600x900.jpg');
                margin-bottom: 2rem;
            }
            .card-6 {
                background-image: url('../assets/img/blog-post2-400x600.jpg');
            }
            .card-1, .card-4 {
                padding-top: calc((80rem - 4rem) / 4);
            }
            .card-2, .card-3, .card-5, .card-6 {
                padding-top: calc((80rem - 0rem) / 2);
            }
        }
        .all-news.my_btn {
            text-align: center;
            border-radius: 0;
            width: 100%;
        }
    }
    // main container music
    .main-container.music {
        background-color: $backgroundMusicIsLife;
    }
    .main-container.music::before {
        content: '';
        width: 260px;
        height: 7px;
        background-color: $mandy;
        display: inline-block;
        position: absolute;
        top: 0;
        left: 50%;
        transform: translateX(-50%);
    }
    // video container
    .video-container {
        background-image: url('../assets/img/home-testimonial-parallax.jpg');
        background-position-y: 50%;
        .w-30 {
            width: 30%;
        }
        .video-content {
            text-align: center;
            color: $white;
            font-style: italic;
            line-height: 1.8em;
            // font-family: $fontFamily;
            padding: 7em 0;
            img {
                width: 15%;
                cursor: pointer;
            }
        }
        .youtube-container {
            z-index: 99;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            .my_btn {
                z-index: 999;
                position: absolute;
                top: 0;
                right: 0;
                margin: 2em;
                
            }
            .frame {
                z-index: 900;
            }
            &.not-active {
                display: none;
            }
            &.active {
                display: flex;
            }
            &:before {
                display: block;
                position: absolute;
                top: 0;
                left: 0;
                content: '';
                height: 100vh;
                width: 100%;
                background-color: $text;
                opacity: 0.7;
            }
        }
    }
</style>