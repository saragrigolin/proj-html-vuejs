<template>
    <main>
        <div class="music-is-life py-5">
            <div class="container-music d-flex justify-content-center flex-column w-50">
                <div class="title-container">
                    <h2 class="title">Music Is Life</h2>
                </div>
                <div class="subtitle-container mt-3 pt-4">
                    <span class="subtitle">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quam alias repudiandae quisquam laboriosam natus, ut accusantium impedit maxime.</span>
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
    .music-is-life {
        background-color: $backgroundMusicIsLife;
        text-align: center;
        color: $white;
        position: relative;
        .container-music {
            margin: 0 auto;
            .title-container {
                font-weight: 700;
            }
            .subtitle-container::before {
                content: '';
                width: 260px;
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
                font-size: 0.8em;
            }
            }
        }
    }
    .music-is-life::before {
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
</style>