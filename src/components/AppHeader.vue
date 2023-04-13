<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                },
            ]
        }
    }
}
</script>

<template>
    <header class="header-box">
        <div class="left">
            <a href="">
                <img src="../assets/img/dc-logo.png" alt="">
            </a>
        </div>
        <nav class="right">
            <ul class="nav-list">
                <li v-for="link in links" :class="link.current ? 'active' : ''">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.header-box {
    @include flex(row, space-around, center);
    width: $width;
    margin: 0 auto;
    height: 140px;

    img {
        margin: 20px;
    }

    .right {


        ul {
            @include flex(row, space-between, center);
            list-style: none;

            li {
                margin: 0 10px;


                a {
                    text-decoration: none;
                    font-weight: 700;
                    color: inherit;
                }

                &.active,
                &:hover {
                    color: $primary;
                    border-bottom: 5px solid $primary;
                }
            }
        }
    }
}
</style>