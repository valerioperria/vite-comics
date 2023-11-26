<script>
export default {
    data() {
        return {
            follows: [
                {
                    platform: 'facebook.png',
                },
                {
                    platform: 'twitter.png',
                },
                {
                    platform: 'youtube.png',
                },
                {
                    platform: 'pinterest.png',
                },
                {
                    platform: 'periscope.png',
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(`../assets/img/footer-${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="container">
        <button><span><strong>SIGN-UP NOW</strong></span></button>
        <div class="follow">
            <h3>FOLLOW US</h3>
            <ul>
                <li v-for="item in follows">
                    <img :src="getImagePath(item.platform)">
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.container {
    width: 100%;
    height: 140px;
    @include flexCenter;
    padding: $generalPadding;
    background-color: rgba(0, 0, 0, 0.867);
    justify-content: space-between;

    button {
        padding: 1rem;
        color: white;
        background-color: rgba(0, 0, 0, 0);
        border: 2px solid $primaryColor;
    }

    ;

    .follow {
        @include flexCenter;

        h3 {
            color: $primaryColor;
            margin-right: 1rem;
        }

        ul {
            @include flexCenter;
            list-style: none;

            li {
                padding: 0.5rem
            }
        }
    }

    ;
}</style>