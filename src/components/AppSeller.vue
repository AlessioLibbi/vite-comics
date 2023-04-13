<script>
export default {
    name: "AppSeller",
    data() {
        return {
            seller: [
                {
                    name: "DIGITAL COMICS",
                    img: "buy-comics-digital-comics.png",
                    url: "#"
                },
                {
                    name: "DC MERCHANDISE",
                    img: "buy-comics-merchandise.png",
                    url: "#"
                },
                {
                    name: "SUBSCRIPTION",
                    img: "buy-comics-subscriptions.png",
                    url: "#"
                },
                {
                    name: "COMIC SHOP LOCATOR",
                    img: "buy-comics-shop-locator.png",
                    url: "#"
                },
                {
                    name: "DC POWER VISA",
                    img: "buy-dc-power-visa.svg",
                    url: "#"
                },
            ]
        }
    },
    methods: {
        getImgPath(item) {

            return new URL(`../assets/img/${item.img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="seller-box">
        <div class="seller-container">
            <ul>
                <li v-for="sell in seller">
                    <a :href="sell.url">
                        <img :src="getImgPath(sell)" alt="">
                        <p>{{ sell.name }}</p>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.seller-box {
    background-color: $primary;
    height: 170px;
    margin: 0 auto;
    position: relative;
    z-index: 10;

    .seller-container {
        margin: 0 auto;
        width: $width;


        ul {
            @include flex(row, space-between, center);
            list-style: none;
            height: 170px;

            li {
                color: white;

                a {
                    @include flex(row, space-between, center);
                    text-decoration: none;
                    font-weight: 700;
                    color: inherit;
                    font-size: 1rem;

                    img {
                        width: 50px;
                        padding: 5px;
                    }
                }
            }
        }
    }
}
</style>