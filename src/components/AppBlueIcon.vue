<script>
export default {
    data() {
        return {
            blueIcon: [
                {
                    icon: 'img/buy-comics-digital-comics.png',
                    title: 'Digital Comics'
                }, {
                    icon: 'img/buy-comics-merchandise.png',
                    title: 'DC Merchandise'
                }, {
                    icon: 'img/buy-comics-subscriptions.png',
                    title: 'Subscriptions'
                }, {
                    icon: 'img/buy-comics-shop-locator.png',
                    title: 'Comics Shop Locator'
                }, {
                    icon: 'img/buy-dc-power-visa.svg',
                    title: 'DC Power Visa'
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="container-inner">

            <div v-for="element in blueIcon" class="blue-icon">

                <img :src="element.icon" alt="">
                <span>{{ element.title }}</span>

            </div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    display: flex;
    justify-content: center;

    width: 100%;
    padding: 2em 1em;
    background: rgb(2, 130, 249);
    color: rgb(254, 254, 254);

    .container-inner {
        width: 100%;
        max-width: 1200px;
        padding: 1em 0;

        display: flex;
        align-items: center;
        justify-content: space-between;

        .blue-icon {
            display: flex;
            align-items: center;
            gap: .5em;

            img {
                width: 60px;
                height: 60px;
                object-fit: contain;
            }

        }

    }
}
</style>