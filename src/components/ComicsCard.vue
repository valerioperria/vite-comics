<script>
export default {
    props: {
        title: String,
        image: String,
    },
};
</script>

<template>
    <div class="card">
        <img :src="image" alt="" />
        <span>{{ title }}</span>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.card {
    display: flex;
    flex-direction: column;

    img {
        width: 160px;
        height: 160px;
    }

    span {
        max-width: 160px;
    }
}</style>