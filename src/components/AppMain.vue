<template>
    <main>
        <div class="jumbo">
            <img src="../assets/img/jumbotron.jpg" alt="Image Titans">
        </div>
        <section>
            <span>
                Current Series
            </span>
            <div class="items">
                <Card v-for="element in arrayComics" :object=element />
            </div>
            <div class="button">
                <button>LOAD MORE</button>
            </div>
        </section>
        <div class="informations">
            <section>
                <Information v-for="element in arrayInformation" :objectInformation="element" />
            </section>
        </div>
    </main>
</template>
<script>
import Card from './Card.vue';
import Information from './Information.vue';
export default {
    components: {
        Card,
        Information,
    },
    name: 'AppMain',
    data() {
        return {
            arrayComics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ],

            arrayInformation: [
                {
                    "image": "../../src/assets/img/buy-comics-digital-comics.png",
                    "text": "digital comics",
                },

                {
                    "image": "../../src/assets/img/buy-comics-merchandise.png",
                    "text": "dc merchandise",
                },

                {
                    "image": "../../src/assets/img/buy-comics-subscriptions.png",
                    "text": "subscription",
                },

                {
                    "image": "../../src/assets/img/buy-comics-shop-locator.png",
                    "text": "comic shop locator",
                },

                {
                    "image": "../../src/assets/img/buy-dc-power-visa.svg",
                    "text": "dc power visa",
                },
            ],
        }
    },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

main {
    color: $primary_color;
    background-color: $black_color;
    font-family: $font;
}

.jumbo {
    height: 300px;
    overflow: hidden;

    img {
        width: 100%;
        display: block;
    }
}

section {
    @include contain;
    @include distance_section;
    position: relative;

    span {
        position: absolute;
        bottom: 97%;
        left: 2.5rem;
        padding: .5rem 1.5rem;
        background-color: $light_blue_color;
        font-weight: bold;
        text-transform: uppercase;
    }
}

.informations {
    background-color: $light_blue_color;

    section {
        display: flex;
        justify-content: space-around;
    }
}

.items {
    padding: 1rem 3rem;
    display: flex;
    flex-wrap: wrap;
}

.button {
    display: flex;
    justify-content: center;
    align-items: center;

    button {
        padding: .5rem 1.5rem;
        background-color: $light_blue_color;
        color: $primary_color;
        font-size: .8rem;
        font-weight: 600;
    }
}
</style>