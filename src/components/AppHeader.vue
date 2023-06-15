<template>
    <header>
        <section>
            <div>
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <nav>
                <ul>
                    <li v-for="element in navBarList">
                        <a v-bind:class="element.active ? 'active' : 'no_active'" href="#">
                            {{ element.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </section>
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
            active: "active",
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

.active {
    color: $active_color;
    border-bottom: 5px solid $active_color;
}

.no_active {
    color: $black_color;
}

section {
    @include contain;
    @include flex_bet;
    font-family: $font;
}

img {
    height: 70px;
    display: $display_block;
    margin: 1rem;
}

nav {
    ul {
        display: $display_flex;
        height: 100%;

        li {
            @include flex_center;
            @include navbar_font_characters;

            a {
                @include flex_center;
                height: 100%;
            }

        }
    }
}
</style>