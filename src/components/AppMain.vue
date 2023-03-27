<script>
import AppCardComics from '../components/AppCardComics.vue';

export default {
    data() {
        return {
            title: "-->Content goes Here<--",

            ComicsList: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
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
            <AppCardComics class="card" v-for="comic in ComicsList" :title="comic.series" :imgsrc="''">
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

        box-shadow: inset 0px 0px 2px rgba(0, 0, 0, 0);

        transition: all .6s;

        &-close {
            max-height: 20px;

            box-shadow: inset 0px -10px 8px rgba(0, 0, 0, 0.5);
        }

    }

}
</style>