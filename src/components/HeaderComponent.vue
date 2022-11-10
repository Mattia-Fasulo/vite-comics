<template>
    <header>
        <div class="container">
            <div class="logo">
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="dc logo">
                </a>
            </div>
            <div class="navbar">
                <nav>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            links: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Video",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ],
        }
    }


}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


.container {
    @include center('horizontal');
    justify-content: space-between;
    height: 120px;

}

.logo {
    height: 100%;
    padding: 1rem;

    img {
        height: 100%;

    }
}

.navbar {

    ul {
        @include center();

        li {
            list-style: none;
            margin: 0.5rem;

            a {
                text-decoration: none;
                text-transform: uppercase;
                color: $light-black;
                font-size: 1rem;
                font-weight: 600;
            }
        }
    }
}
</style>