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

        <div class="container-bottom-footer">
            <div class="inner-bottom-footer">
                <button class="btn btn-footer">SING-UP NOW!</button>

                <div class="icon-social-wrapper">
                    <span>FOLLOW US</span>

                    <img src="/img/footer-facebook.png" alt="">
                    <img src="/img/footer-periscope.png" alt="">
                    <img src="/img/footer-pinterest.png" alt="">
                    <img src="/img/footer-twitter.png" alt="">
                    <img src="/img/footer-youtube.png" alt="">
                </div>
            </div>
        </div>

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

    .inner-bottom-footer {
        width: 100%;
        max-width: 1200px;

        display: flex;
        justify-content: space-between;
        align-items: center;

        .btn {
            padding: .7em 1em;
            cursor: pointer;

            &-footer {
                background: transparent;
                border: 2px solid rgb(2, 130, 249);

                &:hover {
                    background: #0000002c;
                    box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.189);
                }
            }
        }


        .icon-social-wrapper {
            height: 100%;
            display: flex;
            align-items: center;

            gap: 1em;

            span {
                font-size: 1.1em;
                font-weight: 700;
                color: rgb(2, 130, 249);
                padding-right: .4em;
            }
        }
    }
}
</style>