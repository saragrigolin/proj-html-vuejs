<template>
    <ul class="date-list p-0 w-80">
        <li v-for="(date, index) in dates" :key="index" class="date-list-item" type="button" data-bs-toggle="collapse" :data-bs-target="`#collapse${index}`" aria-expanded="false" :aria-controls="`#collapse${index}`">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>{{date.whereWhen}}</span>
            </div>
            <div class="collapse" :id="`collapse${index}`">
                <div class="details d-flex">
                    <img class="p-3" :src="date.img" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            {{date.detailsTitle}}
                        </span>
                        <span class="details-text py-5">{{date.detailsText}}</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li>
        <!-- <li class="date-list-item" type="button" data-bs-toggle="collapse" data-bs-target="#collapse1" aria-expanded="false" aria-controls="collapse1">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>17/08/2020 gem festival 2020 anakalia, georgia</span>
            </div>
            <div class="collapse" id="collapse1">
                <div class="details d-flex">
                    <img class="p-3" src="https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            Untold Stories
                        </span>
                        <span class="details-text py-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li>
        <li class="date-list-item" type="button" data-bs-toggle="collapse" data-bs-target="#collapse2" aria-expanded="false" aria-controls="collapse2">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>24/09/2020 groovegest dominical republic</span>
            </div>
            <div class="collapse" id="collapse2">
                <div class="details d-flex">
                    <img class="p-3" src="https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            Untold Stories
                        </span>
                        <span class="details-text py-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li>
        <li class="date-list-item" type="button" data-bs-toggle="collapse" data-bs-target="#collapse3" aria-expanded="false" aria-controls="collapse3">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>31/10/2020 oasis festival 2020 marrakech, marocco</span>
            </div>
            <div class="collapse" id="collapse3">
                <div class="details d-flex">
                    <img class="p-3" src="https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            Untold Stories
                        </span>
                        <span class="details-text py-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li>
        <li class="date-list-item" type="button" data-bs-toggle="collapse" data-bs-target="#collapse4" aria-expanded="false" aria-controls="collapse4">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>07/11/2020 moga festival - essaouria, marocco</span>
            </div>
            <div class="collapse" id="collapse4">
                <div class="details d-flex">
                    <img class="p-3" src="https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            Untold Stories
                        </span>
                        <span class="details-text py-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li>
        <li class="date-list-item" type="button" data-bs-toggle="collapse" data-bs-target="#collapse5" aria-expanded="false" aria-controls="collapse5">
            <div class="li-header">
                <i class="fas fa-plus"></i><span>10/12/2020 envision festival - uvita, costa rica</span>
            </div>
            <div class="collapse" id="collapse5">
                <div class="details d-flex">
                    <img class="p-3" src="https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2" alt="">
                    <div class="details-content justify-content-end p-3 d-flex flex-column">
                        <span class="details-title">
                            Untold Stories
                        </span>
                        <span class="details-text py-5">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?</span>
                        <button type="button" class="my_btn btn w-25">book now</button>
                    </div>
                </div>
            </div>
        </li> -->
    </ul>
</template>

<script>
export default {
    name: "LiveDates",
    data(){
        return {
            dates: [
                {
                    whereWhen: '17/08/2020 gem festival 2020 anakalia, georgia',
                    img: 'https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2',
                    detailsTitle: 'Untold Stories',
                    detailsText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?'
                },
                {
                    whereWhen: '24/09/2020 groovegest dominical republic',
                    img: 'https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2',
                    detailsTitle: 'Untold Stories',
                    detailsText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?'
                },
                {
                    whereWhen: '31/10/2020 oasis festival 2020 marrakech, marocco',
                    img: 'https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2',
                    detailsTitle: 'Untold Stories',
                    detailsText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?'
                },
                {
                    whereWhen: '07/11/2020 moga festival - essaouria, marocco',
                    img: 'https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2',
                    detailsTitle: 'Untold Stories',
                    detailsText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?'
                },
                {
                    whereWhen: '10/12/2020 envision festival - uvita, costa rica',
                    img: 'https://maps.googleapis.com/maps/api/staticmap?key=AIzaSyDsUcTjt43mTheN9ruCsQVgBE-wgN6_AfY&language=en&center=New+York&maptype=terrain&zoom=14&size=370x250&markers=icon:https://avada.theme-fusion.com/music/wp-content/uploads/sites/68/2017/09/custom_marker-1.png|New+York&scale=2',
                    detailsTitle: 'Untold Stories',
                    detailsText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus vero perspiciatis facilis exercitationem voluptates repudiandae at saepe cum cupiditate! Accusamus ex, voluptate hic et debitis ipsa in sequi tenetur tempora?'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import "../assets/scss/style.scss";
// sezione date
.date-list {
    list-style-type: none;
    margin: 0 auto;
    .date-list-item {
        padding: 1em 1.5em;
        margin-bottom: 0.5em;
        background-color: $backgroundMusicIsLife;
        cursor: pointer;
        .li-header {
            text-transform: uppercase;
            display: flex;
            align-items: center;
            span {
                color: $mandy;
                margin-left: 0.5em;
                font-size: 2em;
            }
            .fa-plus {
                font-size: 1.5em;
                padding: 0.2em;
            }
        }
        .details {
            img {
                width: 33%;
            }
            .details-title {
                font-size: 1.5em;
                font-weight: 300;
            }
            .details-text {
                color: $text;
            }
        }
    }
    .date-list-item:hover {
        background-color: $liHover;
        transition: background-color 0.5s linear;
        .fa-plus {
            background-color: $mandy;
            transition: background-color 0.5s linear;
        }
    }
}
</style>