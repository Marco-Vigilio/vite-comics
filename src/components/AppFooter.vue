<template>
    <footer>
        <section class="principal">
            <div class="container list">
                <div>
                    <ul>
                        <li>Dc comics</li>
                        <li>Characters</li>
                        <li>Comix</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>

                    <ul>
                        <li>Shop</li>
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>DC</li>
                        <li>Terms Of Us</li>
                        <li>Privacy policy (New)</li>
                        <li>Ad Choices</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscriptions</li>
                        <li>Talent Workshops</li>
                        <li>CPSC Certificates</li>
                        <li>Ratings</li>
                        <li>Shop Help</li>
                        <li>Contact Us</li>
                    </ul>
                </div>
                <div>
                    <ul>
                        <li>Sites</li>
                        <li>DC</li>
                        <li>MAD Magazine</li>
                        <li>DC Kids</li>
                        <li>DC Universe</li>
                        <li>DC Power Visa</li>
                    </ul>
                </div>
                <img src="../assets/img/dc-logo-bg.png" alt="Logo DC">
            </div>
        </section>
        <section class="second">
            <div class="container functions">
                <div>
                    <button>sign-up now</button>
                </div>
                <div class="follow">
                    <span>FOLLOW US</span>
                    <ul>
                        <li><img src="../assets/img/footer-facebook.png" alt="Logo facebook"></li>
                        <li><img src="../assets/img/footer-twitter.png" alt="Logo twitter"></li>
                        <li><img src="../assets/img/footer-youtube.png" alt="Logo youtube"></li>
                        <li><img src="../assets/img/footer-pinterest.png" alt="Logo pinterest"></li>
                        <li><img src="../assets/img/footer-periscope.png" alt="Logo periscope"></li>
                    </ul>
                </div>

            </div>
        </section>
    </footer>
</template>
<script>
export default {
    name: 'AppFooter',
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer {
    color: $primary_color;
    font-family: $font;
}

.principal {
    background: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    overflow: hidden;
}

.second {
    background-color: $gray_color;
}

div .container {
    @include contain;
    @include distance_section;

}

.list {
    display: flex;
    position: relative;
    color: gray;


    ul {
        margin-right: 2rem;

        li:first-child {
            font-size: 1.5rem;
            margin: .83rem 0;
            color: $primary_color;
            text-transform: uppercase;
            font-weight: 600;
        }

        li:hover {
            color: $primary_color;
            cursor: pointer;
        }
    }

    img {
        top: 50%;
        right: 0;
        transform: translateY(-50%);
        position: absolute;
        height: 500px;

    }
}

.functions {
    @include flex_bet;

    button {
        height: 100%;
        padding: .8rem;
        color: $primary_color;
        border: 2px solid $light_blue_color;
        text-transform: uppercase;
        cursor: pointer;

    }

    .follow {
        @include flex_center;

        span {
            margin: 0 2rem;
            color: $light_blue_color;
            font-size: 600;
        }

        ul {
            @include flex_center;

            li {
                margin-left: 1rem;
                cursor: pointer;

                img {
                    height: 30px;
                }
            }
        }
    }
}
</style>