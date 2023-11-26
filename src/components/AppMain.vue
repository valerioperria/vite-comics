<script>
export default {
    data() {
        return {
            items: [
                {
                    title: 'DC COMICS',
                    list: [
                        { name: 'Characters' },
                        { name: 'Comics' },
                        { name: 'Movies' },
                        { name: 'TV' },
                        { name: 'Games' },
                        { name: 'Videos' },
                        { name: 'News' },
                    ]
                },
                {
                    title: 'SHOP',
                    list: [
                        { name: 'Shop DC' },
                        { name: 'Shop DC Collectibles' },
                    ]
                },
                {
                    title: 'DC',
                    list: [
                        { name: 'Terms Of Use' },
                        { name: 'Privacy policy (New)' },
                        { name: 'Ad Choice' },
                        { name: 'Advertising' },
                        { name: 'Jobs' },
                        { name: 'Subscription' },
                        { name: 'Talent Workshop' },
                        { name: 'CPSC Certificates' },
                        { name: 'Ratings' },
                        { name: 'Shop Help' },
                        { name: 'Contact Us' },
                    ]
                },
                {
                    title: 'SITES',
                    list: [
                        { name: 'DC' },
                        { name: 'MAD Magazine' },
                        { name: 'DC Kids' },
                        { name: 'DC Universe' },
                        { name: 'DC Power Visa' },
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <div class="title" v-for="item in items" :key="item.title">
                <h3>{{ item.title }}</h3>
                <ul>
                    <li v-for="names in item.list"><a href="">{{ names.name }}</a></li>
                </ul>
            </div>
        </div>
        <div class="dc"></div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.container {
    width: 100%;
    height: 370px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    padding: $generalPadding;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .wrapper {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        height: 100%;
        width: 35%;
        padding: 2rem 0;

        .title {
            margin-bottom: 1rem;

            h3 {
                color: white;
                margin-bottom: 1rem;
            }

            li {
                list-style: none;
                margin-bottom: 0.2rem;

                a {
                    text-decoration: none;
                    color: grey;
                }
            }
        }

    }

    .dc {
        width: 40%;
        height: 100%;
        background-image: url(../assets/img/dc-logo-bg.png);
        background-size: cover;
        background-position: center;
    }

}
</style>