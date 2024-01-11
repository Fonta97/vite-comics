<script>
import ProductCard from './ProductCard.vue';
export default {
    name: 'ListProducts',
    components: {
        ProductCard,
    },
    data() {
        return {
            products: [
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
            cards: [
                {
                    text: 'DIGITAL COMICS',
                    img: 'public/img/card/buy-comics-digital-comics.png',
                    url: '#',
                    current: true,
                },
                {
                    text: 'DC MERCHANDISE',
                    img: 'public/img/card/buy-comics-merchandise.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'SUBSCRIPTION',
                    img: 'public/img/card/buy-comics-shop-locator.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    img: 'public/img/card/buy-comics-subscriptions.png',
                    url: '#',
                    current: false,
                },
                {
                    text: 'DC POWER VISA',
                    img: 'public/img/card/buy-dc-power-visa.svg',
                    url: '#',
                    current: false,
                }
            ]
        }
    }
}
</script>

<template>
    <section id="jumbotron">
        <img class="fill" src="../../public/img/jumbotron.jpg" alt="">
    </section>
    <main>
        <div class="container">
            <!-- __> Content goes here &lt;__ -->
            <div class="btn">
                <h3>CURRENT SERIES</h3>
            </div>
            <div class="row">
                <!-- codice componente card prodotto -->
                <ProductCard v-for="(product, idx) in products" :key="idx" :details="product" />
            </div>
            <div class="btn center">
                <h3>
                    <a href="">LOAD MORE</a>
                </h3>
            </div>
        </div>
    </main>
    <section>
        <div class="container">
            <ul>
                <li v-for="card in cards">
                    <a :href="card.url">
                        <img :src="card.img" alt="">
                        <span>{{ card.text }}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
// SCSS ONLY COMPONENT
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

h1,
h2,
h3,
h4,
h5,
h6 {
    color: $light;
}

main {
    background-color: #1c1c1c;
    padding: 2rem 0;

    .row {
        display: flex;
        padding: 0.5rem 0.5rem;
        flex-wrap: wrap;
    }

    .btn {
        background-color: #0282f9;
        width: fit-content;
        padding: 1rem 0.5rem;
        position: relative;
        bottom: 4rem;

        &.center {
            bottom: 0;
            margin: 0 auto;

            h3 {
                font-size: 1rem;

                a {
                    color: $light;
                    text-decoration: none;
                }

            }

            &:hover {
                background-color: #558cc0;
            }
        }
    }
}

section {
    background-color: #0282f9;

    &#jumbotron {
        background-color: #1c1c1c;

        img {
            width: 100%;
            height: 500px;

            &.fill {
                object-fit: cover;
                object-position: top;
            }
        }
    }


    ul {

        list-style: none;
        @include center();
        display: flex;
        width: 100%;

        li {
            width: calc(100% / 5);
            height: fit-content;

        }

        li a {
            padding: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: nowrap;
            text-decoration: none;
            font-weight: 600;
            color: $light;
            @include center();

            img {
                max-width: 30%;
                margin-right: 10px;
            }
        }
    }
}
</style>