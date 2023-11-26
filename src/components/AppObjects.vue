<script>
export default {
    data() {
        return {
            objects: [
                {
                    name: 'DIGITAL COMICS',
                    object: 'comics-digital-comics.png',
                },
                {
                    name: 'DC MERCHANDISE',
                    object: 'comics-merchandise.png',
                },
                {
                    name: 'SUBSCRIPTION',
                    object: 'comics-subscriptions.png',
                },
                {
                    name: 'COMIC SHOP LOCATOR',
                    object: 'comics-shop-locator.png',
                },
                {
                    name: 'DC POWER VISA',
                    object: 'dc-power-visa.svg',
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/buy-${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="container">
        <ul>
            <li v-for="item in objects">
                <img :src="getImagePath(item.object)" alt="">
                <span>{{ item.name }}</span>
            </li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.container {
    background-color: $primaryColor;
    color: white;
    width: 100%;
    height: 140px;
    padding: 0 320px;
    @include flexCenter;

    ul {
        @include flexCenter;
        list-style-type: none;
        justify-content: space-between;
        width: 100%;

        li {
            @include flexCenter;

            img {
                height: 3rem;
                margin-right: 1rem;
            }
        }
    }
}
</style>