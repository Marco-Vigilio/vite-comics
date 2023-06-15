<template>
    <header>
        <div class="contain">
            <div>
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <nav>
                <ul>
                    <li v-for="element in navBarList">
                        {{ element.text }}
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>
<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            navBarList: [
                {
                    text: "characters",
                    active: false,
                },

                {
                    text: "comics",
                    active: true,
                },

                {
                    text: "movies",
                    active: false,
                },

                {
                    text: "tv",
                    active: false,
                },

                {
                    text: "games",
                    active: false,
                },

                {
                    text: "collectibles",
                    active: false,
                },

                {
                    text: "videos",
                    active: false,
                },

                {
                    text: "fans",
                    active: false,
                },

                {
                    text: "news",
                    active: false,
                },

                {
                    text: "shop",
                    active: false,
                },
            ],
        }
    },

    methods: {
        getImagePath: function (img) {
            return new URL('./');
        },
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
</style>