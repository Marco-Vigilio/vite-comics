<template>
    <div class="item">
        <div class="image">
            <img :src="object.thumb" alt="">
        </div>
        <div class="description">
            <p>{{ object.series }}</p>
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
    margin: 1rem .5rem;

    .image {
        height: 160px;
        background-color: rgb(11, 255, 174);
        overflow: hidden;

        img {
            width: 100%;
            display: block;
        }
    }

    .description {
        margin: 1rem 0;

        p {
            text-transform: uppercase;
            font-size: .70rem;
        }
    }
}
</style>