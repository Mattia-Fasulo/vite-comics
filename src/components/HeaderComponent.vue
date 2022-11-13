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
                            <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                        </li>
                    </ul>
                </nav>
                <i class="fa-solid fa-bars"></i>
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
    i {
        cursor: pointer;
        color: $blu;
        font-size: 2.5rem;
        display: none
    }

    ul {
        @include center();

        li {
            list-style: none;
            padding: 5px 15px;
            position: relative;

            a {
                text-decoration: none;
                text-transform: uppercase;
                color: $light-black;
                font-size: 0.8rem;
                font-weight: 600;
            }

            &:hover,
            .active {

                &::after {
                    content: '';
                    position: absolute;
                    top: 70px;
                    right: 0;
                    width: 100%;
                    height: 5px;
                    background-color: $blu;
                }
            }
        }
    }
}

@media screen and (max-width: 870px) {
    .container {
        margin: 0 50px;
    }

    .navbar {
        i {
            display: block
        }

        nav {
            display: none;
        }
    }
}
</style>