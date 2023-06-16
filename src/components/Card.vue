<template>
    <div class="item">
        <div class="image">
            <img :src="object.thumb" alt="">
        </div>
        <div class="description">
            <span>{{ object.series }}</span>
        </div>

    </div>
</template>
<script>
export default {
    name: "Card",
    props: {
        object: Object,
    },
}
</script>
<style lang="scss" scoped>
.item {
    width: calc((100% / 6) - 1rem);
    background-color: red;
    border: 2px solid black;
    margin: 1rem .5rem;

    .image {
        height: 200px;
        background-color: aquamarine;

        img {
            width: 100%;
            display: block;
        }
    }
}
</style>