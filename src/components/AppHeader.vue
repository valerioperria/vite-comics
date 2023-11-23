<script>
export default {
    data() {
        return {
            navTitles: [
                {
                    title: "CHARACTERS",
                },
                {
                    title: "COMICS",
                },
                {
                    title: "MOVIES",
                },
                {
                    title: "TV",
                },
                {
                    title: "GAMES",
                },
                {
                    title: "COLLECTIBLES",
                },
                {
                    title: "VIDEOS",
                },
                {
                    title: "FANS",
                },
                {
                    title: "NEWS",
                },
                {
                    title: "SHOP",
                },
            ],
        };
    },
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="" />
            </div>
            <nav>
                <ul>
                    <li v-for="titles in navTitles" :key="titles.title">
                        <a href=""><strong>{{ titles.title }}</strong></a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.container {
    width: 100%;
    height: 140px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 100px;

    ul {
        display: flex;

        li {
            list-style: none;
            padding: 0 1rem;
            height: 140px;
            display: flex;
            justify-content: space-between;
            align-items: center;

            &:hover {
                border-bottom: 5px solid $primaryColor;
            }

            a {
                text-decoration: none;
                color: black;
            }
        }
    }
}
</style>