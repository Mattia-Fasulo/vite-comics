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
                        <li v-for="(link, index) in navbar" :key="index">
                            <a :href="link.url">{{ link.text }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
import { links } from '../data/links.js'
export default {
    name: 'HeaderComponent',
    data() {
        return {
            navbar: links,
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
    padding: 1rem 0;

    img {
        height: 100%;

    }
}

.navbar {

    ul {
        @include center();

        li {
            list-style: none;
            padding: 5px 15px;

            a {
                text-decoration: none;
                text-transform: uppercase;
                color: $light-black;
                font-size: 0.8rem;
                font-weight: 600;
            }
        }
    }
}
</style>