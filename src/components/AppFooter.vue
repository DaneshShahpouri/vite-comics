<script>
export default {
    data() {
        return {
            FooterLinks: [
                {
                    name: 'DC Comincs',
                    links: [
                        "Characters",
                        "Comics",
                        "Movies",
                        "Tv",
                        "Games",
                        "Videos",
                        "News",
                    ]
                }, {
                    name: 'Shop',
                    links: [
                        "Shop DC",
                        "Shop DC Collectibles",
                    ]
                }, {
                    name: 'Terms Of Use',
                    links: [
                        "Privacy Police (news)",
                        "Ad Choices",
                        "Advertising",
                        "Jobs",
                        "Subscriptions",
                        "Talent Workshops",
                        "CPSC Cerficates",
                        "Ratings",
                        "Shop Help",
                        "Contact Us",
                    ]
                }, {
                    name: 'Sites',
                    links: [
                        "Dc",
                        "MAD Magazine",
                        "DC Kids",
                        "DC Universe",
                        "DC Power Visa",
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <footer>

        <div class="container-top-footer">
            <div class="inner-top-footer">

                <div class="links-container">
                    <ul v-for="section in FooterLinks">
                        <li class="main-li">{{ section.name }}</li>
                        <ul>
                            <li v-for="link in section.links">
                                {{ link }}
                            </li>
                        </ul>
                    </ul>
                </div>

            </div>
        </div>

        <div class="container-bottom-footer"></div>

    </footer>
</template>

<style lang="scss" scoped>
.container-top-footer {
    display: flex;
    justify-content: center;
    width: 100%;
    background-image: url(./img/footer-bg.jpg);
    height: 360px;
    position: relative;

    &::before {
        content: '';
        background-image: url(./img/dc-logo-bg.png);
        background-position: center;
        background-size: cover;
        width: 360px;
        height: 100%;
        position: absolute;
        right: 20px;
        top: 0px;
    }

    .inner-top-footer {
        height: 100%;
        width: 100%;
        max-width: 1200px;

        .links-container {
            height: 100%;
            width: 400px;
            display: flex;
            flex-direction: column;
            align-content: space-around;
            flex-wrap: wrap;

            ul {
                margin: .5em 0;

                .main-li {
                    font-weight: 800;
                    font-size: 1.2em;
                    margin-bottom: .6em;
                    color: white;
                    cursor: auto;

                    &:hover {
                        font-weight: 800;
                        font-size: 1.2em;
                        margin-bottom: .6em;
                    }
                }

                li {

                    list-style-type: none;
                    font-weight: 100;
                    font-size: .9em;
                    color: rgb(176, 176, 176);
                    cursor: pointer;

                    &:hover {
                        color: white;
                        text-shadow: 1px 1px 2px black;
                        font-weight: 200;
                    }
                }
            }
        }
    }
}

.container-bottom-footer {
    display: flex;
    justify-content: center;
    width: 100%;
    background: rgb(48, 48, 48);

    height: 100px;

}
</style>