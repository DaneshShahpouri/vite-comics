<script>
import AppCardComics from '../components/AppCardComics.vue';

export default {
    data() {
        return {
            title: "-->Content goes Here<--",

            ComicsList: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ],

            isShow: true

        }
    },

    components: {
        AppCardComics,

    },

    methods: {
        toggleClass() {
            if (this.isShow == true) {
                this.isShow = false;
            } else {
                this.isShow = true;
            }
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="jumbo">
            <div class="button-wrapper">
                <button class="btn btn-jumbo-absolute" @click="toggleClass()">Current Series</button>
            </div>
        </div>

        <div class="main-wrapper" :class="isShow == false ? 'main-wrapper-close' : ''">
            <div class="shadows" v-if="isShow == false"></div>
            <AppCardComics class="card" v-for="comic in ComicsList" :title="comic.series" :imgsrc="comic.thumb">
            </AppCardComics>
            <div class="btn btn-jumbo">Load More</div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.btn {
    padding: .7em 1.4em;

    font-size: 1.2em;
    font-weight: 400;

    text-transform: uppercase;

    &-jumbo {
        background-color: rgb(2, 130, 249);
        border: none;
        margin: 1em;
        font-size: .9em;
        padding: .5em 1.9em;

        cursor: pointer;

        transition: all .4s;

        &:hover {
            background-color: darken($color: rgb(2, 130, 249), $amount: 20);
        }

        &:active {
            background-color: lighten($color: rgb(2, 130, 249), $amount: 20);
        }
    }

    &-jumbo-absolute {
        background-color: rgb(2, 130, 249);
        border: none;

        cursor: pointer;

        transition: all .4s;

        position: absolute;
        bottom: 0;
        left: 10px;
        transform: translateY(50%);

        &:hover {
            background-color: darken($color: rgb(2, 130, 249), $amount: 20);
        }

        &:active {
            background-color: lighten($color: rgb(2, 130, 249), $amount: 10);
        }
    }

}

.container {
    width: 100%;

    background: rgb(28, 28, 28);
    color: white;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .jumbo {
        width: 100%;
        height: 300px;

        background-image: url('./img/jumbotron.jpg');
        background-size: cover;

        margin-bottom: 2em;

        .button-wrapper {
            position: relative;
            width: 100%;
            height: 100%;
            max-width: 1200px;
            margin: 0 auto;
        }


    }


    .main-wrapper {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: flex-start;
        align-content: flex-start;
        gap: 1em;

        width: 100%;
        max-width: 1200px;
        max-height: 800px;

        padding: 1em;
        margin: 0 auto;
        margin-bottom: 1em;
        overflow: hidden;

        position: relative;

        // box-shadow: inset 0px 0px 2px rgba(0, 0, 0, 0);

        transition: all .6s;

        &-close {
            max-height: 80px;

            box-shadow: inset 0px -10px 8px rgba(0, 0, 0, 0.5);
        }

        .shadows {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 20px;
            background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 1));
            z-index: 1;

            animation: appeare .5s;
        }


    }

    @keyframes appeare {
        0% {
            opacity: 0;
        }

        100% {
            opacity: 1;
        }

    }

}
</style>