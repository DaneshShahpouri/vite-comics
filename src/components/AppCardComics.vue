<script>
export default {
    name: "AppCardComics",
    data() {
        return {

        }
    },

    props: {
        imgsrc: String,
        title: String,
    },
}
</script>

<template>
    <div class="container-card">
        <div class="img-wrapper">
            <img :src="imgsrc" alt="">
        </div>

        <div class="text-wrapper">
            <span>{{ title }}</span>
        </div>
    </div>
</template>

<style lang="scss">
.container-card {
    width: calc((100% / 6) - ((1em / 6) * 5));
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: .6em;

    opacity: .8;

    cursor: pointer;

    transition: all .4s;



    &:hover {
        opacity: 1;

        .img-wrapper {
            box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.484);
        }

        .text-wrapper {
            padding-right: .1em;

            span {
                border-left: 2px solid rgb(2, 130, 249);
                padding-left: .4em;
            }
        }
    }

    .img-wrapper {
        width: 100%;
        height: 100%;
        aspect-ratio: 1/1;

        box-shadow: 0 0 5px transparent;

        overflow: hidden;
        background: #000;

        transition: all .4s;
    }

    .text-wrapper {
        color: rgb(237, 237, 237);

        padding-right: .5em;

        transition: all .4s;

        span {
            display: inline-block;
            text-transform: uppercase;
            font-size: .95em;

            transition: all .4s;
        }
    }
}
</style>