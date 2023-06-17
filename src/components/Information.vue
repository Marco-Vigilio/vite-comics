<template>
    <div class="item">
        <div class="image"><img :src="objectInformation.image"></div>
        <p>{{ objectInformation.text }}</p>
    </div>
</template>
<script>
export default {
    name: "Information",
    props: {
        objectInformation: Object,
    }
}
</script>
<style lang="scss" scoped>
.item {
    display: flex;
    justify-content: center;
    align-items: center;

    .image {
        width: 40px;

        img {
            width: 100%;
            height: 40px;
            object-fit: contain;
        }
    }

    p {
        text-transform: uppercase;
        font-size: .8rem;
        margin-left: .5rem;
    }
}
</style>