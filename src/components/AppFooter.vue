<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            footerLinks: [
                {
                    title: 'DC COMICS',
                    links: [
                        {
                            text: "Characters",
                            url: "#"
                        }, {
                            text: "Comics",
                            url: "#"
                        }, {
                            text: "Movies",
                            url: "#"
                        }, {
                            text: "TV",
                            url: "#"
                        }, {
                            text: "Games",
                            url: "#"
                        }, {
                            text: "Videos",
                            url: "#"
                        }, {
                            text: "News",
                            url: "#"
                        }
                    ]
                },
                {
                    title: 'SHOP',
                    links: [
                        {
                            text: "Shop DC",
                            url: "#"
                        }, {
                            text: "Shop DC Collectibles",
                            url: "#"
                        }
                    ]
                },
                {
                    title: 'DC',
                    links: [
                        {
                            text: "Terms Of Use",
                            url: "#"
                        }, {
                            text: "Privacy policy (New)",
                            url: "#"
                        }, {
                            text: "Ad Choices",
                            url: "#"
                        }, {
                            text: "Advertising",
                            url: "#"
                        }, {
                            text: "Jobs",
                            url: "#"
                        }, {
                            text: "Subscription",
                            url: "#"
                        }, {
                            text: "Talent Workshops",
                            url: "#"
                        }, {
                            text: "CPSC Certificates",
                            url: "#"
                        }, {
                            text: "Ratings",
                            url: "#"
                        }, {
                            text: "Shop Help",
                            url: "#"
                        }, {
                            text: "Contact Us",
                            url: "#"
                        }
                    ]
                },
                {
                    title: 'SITES',
                    links: [
                        {
                            text: "DC",
                            url: "#"
                        }, {
                            text: "MAD Magazine",
                            url: "#"
                        }, {
                            text: "DC Kids",
                            url: "#"
                        }, {
                            text: "DC Universe",
                            url: "#"
                        }, {
                            text: "DC Power VIsa",
                            url: "#"
                        }
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="main">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <!-- title -->
                        <h3>DC COMICS</h3>
                        <ul>
                            <!-- list item -->
                            <li v-for="(link, idx) in footerLinks[0].links" key="idx">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                        <!-- title -->
                        <h3>SHOP</h3>
                        <ul>
                            <!-- list item -->
                            <li v-for="(link, idx) in footerLinks[1].links" key="idx">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <!-- title -->
                        <h3>DC</h3>
                        <ul>
                            <!-- list item -->
                            <li v-for="(link, idx) in footerLinks[2].links" key="idx">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <!-- title -->
                        <h3>SITES</h3>
                        <ul>
                            <!-- list item -->
                            <li v-for="(link, idx) in footerLinks[3].links" key="idx">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="dc-img"></div>
            </div>
        </section>
        <section class="secondary">
            <div class="container">
                <div class="btn">
                    <a href="">SIGN-UP NOW!</a>
                </div>
                <div class="social">
                    <h2>FOLLOW US</h2>
                    <ul>
                        <li>
                            <a href="">
                                <img src="../../public/img/social/footer-facebook.png" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="">
                                <img src="../../public/img/social/footer-twitter.png" alt="">
                                <img src="" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="">
                                <img src="../../public/img/social/footer-youtube.png" alt="">
                                <img src="" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="">
                                <img src="../../public/img/social/footer-pinterest.png" alt="">
                                <img src="" alt="">
                            </a>
                        </li>
                        <li>
                            <a href="">
                                <img src="../../public/img/social/footer-periscope.png" alt="">
                                <img src="" alt="">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
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

footer {
    section.main {
        background-image: url('../../public/img/social/footer-bg.jpg');
        background-size: cover;

        .container {
            display: flex;
        }

        .row {
            display: flex;
            flex-wrap: nowrap;
            width: 50%;

            .col {
                width: calc(100% / 3) -2rem;
                margin: 1rem;

                h3 {
                    margin: 1rem 0;
                    font-weight: 600;
                }

                ul {
                    list-style: none;
                }

                li {
                    margin: 0.4rem 0;
                }

                li a {
                    text-decoration: none;

                    &:hover {
                        color: $light;
                    }
                }
            }
        }

        .dc-img {
            width: 50%;
            background-image: url('../../public/img/dc-logo-bg.png');
            background-size: cover;
            background-position: center;
        }
    }

    section.secondary {
        background-color: #404040;
        padding: 2rem 0;

        .container {
            display: flex;
            justify-content: space-between;

            @include center('horizontal');

            .btn {
                padding: 1rem;
                border: 3px solid $primary;

                a {
                    text-decoration: none;
                    color: $light;
                }

                &:hover {
                    background-color: $grey;
                }
            }

            .social {
                display: flex;

                h2 {
                    color: $primary;
                    display: block;
                    align-self: center;
                }

                ul {
                    display: flex;
                    list-style: none;

                    li {
                        margin: 0 1rem;
                    }
                }


            }
        }
    }
}
</style>