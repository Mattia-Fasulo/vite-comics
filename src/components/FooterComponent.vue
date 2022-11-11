<template>
    <footer>


        <div class="footer-top">

            <div class="container">
                <div class="footer-list">
                    <div class="col">
                        <h3>Dc Comics</h3>
                        <ul>
                            <li v-for="(link, index) in comics" :key="index">
                                <a href="link.url">{{ link.text }}</a>
                            </li>
                        </ul>
                        <h3>Shop</h3>
                        <ul>
                            <li><a href="#">Shop Dc</a></li>
                            <li><a href="#">Shop Dc Collection</a></li>
                        </ul>

                    </div>
                    <div class="col">
                        <h3>Dc</h3>
                        <ul>
                            <li v-for="(link, index) in dc" :key="index">
                                <a href="link.url">{{ link.text }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <h3>Sites</h3>
                        <ul>
                            <li v-for="(link, index) in sites" :key="index">
                                <a href="link.url">{{ link.text }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="footer-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo footer">

                </div>

            </div>
        </div>
        <div class="footer-bot">
            <div class="container">


            </div>
        </div>



    </footer>
</template>

<script>
export default {
    name: 'FooterComponent',
    data() {
        return {
            comics: [
                {
                    text: "Characters",
                    url: "#",
                },
                {
                    text: "Comics",
                    url: "#",
                },
                {
                    text: "Movies",
                    url: "#",
                },
                {
                    text: "Tv",
                    url: "#",
                },
                {
                    text: "Games",
                    url: "#",
                },

                {
                    text: "Video",
                    url: "#",
                },

                {
                    text: "News",
                    url: "#",
                },
            ],
            dc: [
                {
                    text: "Terms of Use",
                    url: "#",
                },
                {
                    text: "Privacy Police (News)",
                    url: "#",
                },
                {
                    text: "Ad Choise",
                    url: "#",
                },
                {
                    text: "Advertising",
                    url: "#",
                },
                {
                    text: "Jobs",
                    url: "#",
                },

                {
                    text: "Subscriptions",
                    url: "#",
                },

                {
                    text: "Talent Workshop",
                    url: "#",
                },
                {
                    text: "CPSC certification",
                    url: "#",
                },
                {
                    text: "Ratings",
                    url: "#",
                },
                {
                    text: "Shop Help",
                    url: "#",
                },
                {
                    text: "Contact Us",
                    url: "#",
                },
            ],
            sites: [
                {
                    text: "DC",
                    url: "#"
                },
                {
                    text: "Mad Magazine",
                    url: "#"
                },
                {
                    text: "DC Kids",
                    url: "#"
                },
                {
                    text: "DC Universe",
                    url: "#"
                },
                {
                    text: "DC Power Visa",
                    url: "#"
                }

            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

footer {
    color: white;
}

.footer-top {
    position: relative;
    height: 370px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;


    .container {
        @include center('horizontal');
        justify-content: space-between;
    }
}

.footer-list {
    @include center('vertical');
    padding: 30px 0;

    .col {
        margin-right: 50px;
    }

    h3 {
        font-size: 1rem;
        text-transform: uppercase;
        margin: 15px 0;
    }

    ul li {
        list-style: none;
        padding: 3px 0;
        font-size: 0.8rem;

        a {
            text-decoration: none;
            color: grey;
        }
    }
}

.footer-logo {


    img {

        height: 130%;
        position: absolute;
        z-index: 0;
        right: 180px;
        top: -50px;
    }

}

.footer-bot {
    position: relative;
    z-index: 100;
    height: 120px;
    background-color: $light-black;
}
</style>