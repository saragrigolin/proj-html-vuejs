<template>
    <main>
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
        <div class="main-container pt-5">
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
                                <div class="card-1">
                                    <div class="container-text d-flex flex-column p-4">
                                        <span class="card-title">Technology and music</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-6 p-3">
                                <div class="card-2">
                                    <div class="container-text d-flex flex-column p-4">
                                        <span class="card-title">Technology and music</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-6 p-3">
                                <div class="card-3">
                                    <div class="container-text d-flex flex-column p-4">
                                        <span class="card-title">Technology and music</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                </div>
                            </div>
                            <div class="col-12 p-3">
                                <div class="card-4">
                                    <div class="container-text d-flex flex-column p-4">
                                        <span class="card-title">Technology and music</span>
                                        <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-4 p-3">
                        <div class="card-5">
                            <div class="container-text d-flex flex-column p-4">
                                <span class="card-title">Technology and music</span>
                                <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                            </div>
                        </div>
                        <div class="card-6">
                            <div class="container-text d-flex flex-column p-4">
                                <span class="card-title">Technology and music</span>
                                <span class="card-subtitle">Sed sit amet sem turpis. Curabitur cursus lacinia est at interdum risus id condimentum.</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <button class="all-news btn my_btn py-5">
                <span>view all latest news</span>
            </button>
        </div>
        <div class="video-container py-5 d-flex justify-content-center">
            <div class="video-content w-30">
                <p>“I just listened to it and said to myself, “Man, I really love this album.” Still, today, it just sounds so fresh. It sounds full of ideas. These guys knew what they were doing. They’re good. And they’re inventive. I haven’t heard anything this year that’s as inventive. I don’t really expect to.”</p>
                <img src="../assets/img/band_interview_play_icon.png" alt="" class="mt-4">
            </div>
        </div>
        <div class="main-container py-5">
            <div class="main-content d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Live Dates</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
                </div>
            </div>
            <div class="container">
                <ul class="date-list px-0 py-4">
                    <li class="date-list-item"><i class="fas fa-plus"></i><span>17/08/2020 gem festival 2020 anakalia, georgia</span></li>
                    <li class="date-list-item"><i class="fas fa-plus"></i><span>24/09/2020 groovegest dominical republic</span></li>
                    <li class="date-list-item"><i class="fas fa-plus"></i><span>31/10/2020 oasis festival 2020 marrakech, marocco</span></li>
                    <li class="date-list-item"><i class="fas fa-plus"></i><span>07/11/2020 moga festival - essaouria, marocco</span></li>
                    <li class="date-list-item"><i class="fas fa-plus"></i><span>10/12/2020 envision festival - uvita, costa rica</span></li>
                </ul>
            </div>
        </div>


    </main>
</template>

<script>
export default {
    name: "Main",

}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
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
                img {
                    width: 100%;
                }
                .container-text {
                    background-color: $backgroundMusicIsLife;
                    width: 100%;
                    position: absolute;
                    bottom: 0;
                    .card-title {
                        color: $mandy;
                        font-weight: 600;
                    }
                    .card-subtitle {
                        color: $text;
                    }
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
            background-color: $mandy;
            color: $white;
            text-transform: uppercase;
            text-align: center;
            cursor: pointer;
            border-radius: 0;
            width: 100%;
        }
        .all-news.my_btn:hover {
            background-color: $white;
            color: $charade;
        }
    }
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
            }
        }
    }
    .date-list {
        list-style-type: none;
        width: 70%;
        margin: 0 auto;
        .date-list-item {
            text-transform: uppercase;
            padding: 1em 1em;
            margin-bottom: 0.5em;
            display: flex;
            align-items: center;
            background-color: $backgroundMusicIsLife;
            span {
                color: $mandy;
                margin-left: 1em;
            }
            .fa-plus {
                font-size: 0.6em;
            }
        }
    }
</style>