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
        <div class="main-container py-5">
            <div class="main-content d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Latest Band News</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
                </div>
            </div>
            <div class="news-container container pt-5">
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
</style>