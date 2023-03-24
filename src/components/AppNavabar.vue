<script>
export default {
    data() {
        return {
            links: [
                "Character",
                "Comics",
                "Movie",
                "Tv",
                "Games",
                "Collectibles",
                "Video",
                "Fans",
                "News",
                "Shop",
            ],
        }
    }
}
</script>

<template>
    <nav>

        <div class="nav-inner">

            <div class="logo-wrapper">
                <img src="/img/dc-logo.png" alt="">
            </div>

            <ul class="links">
                <li v-for="link in links" class="link">
                    <a href="#">{{ link }}</a>
                </li>
            </ul>
        </div>

    </nav>
</template>

<style  lang="scss" scoped>
@mixin my-display-flex($justifyContent) {
    display: flex;
    flex-direction: row;
    justify-content: $justifyContent;
    align-items: center;
}

nav {
    display: flex;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 100px;

    background: rgb(255, 255, 255);
    padding: 0 1em;


    .nav-inner {
        @include my-display-flex(space-between);

        width: 100%;
        max-width: 1200px;
        height: 100%;

        .logo-wrapper {
            width: 60px;
            height: 60px;

            img {
                width: 100%;
                height: 100%;
                object-fit: cover;
            }
        }

        .links {
            @include my-display-flex(flex-start);
            gap: 10px;
            height: 100%;

            li {
                display: flex;
                align-items: center;
                list-style-type: none;
                height: 100%;
                border-bottom: 4px solid rgba(0, 0, 255, 0);
                color: black;

                &:hover {
                    border-bottom: 4px solid rgb(2, 130, 249);
                    color: rgb(2, 130, 249)
                }

                a {
                    color: inherit;
                    text-decoration: none;
                    text-transform: uppercase;
                    font-size: .8em;
                    font-weight: 600;
                }
            }
        }
    }

}
</style>
