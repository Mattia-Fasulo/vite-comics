<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="(link, index) in menu" :key="index">
                    <div class="img-menu">
                        <a :href="link.url"><img :src="link.img" alt="link.title"></a>
                    </div>
                    <div class="title-menu">
                        <a :href="link.url">{{ link.title }}</a>
                    </div>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
import { menuSection } from '../data/links'
export default {
    name: 'SectionMenu',
    data() {
        return {
            menu: menuSection
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

section {
    background-color: $blu;
    height: 160px;

    .container {
        @include center();
        height: 100%;

        ul {
            @include center();

            li {
                @include center;
                flex-basis: calc(100% / 5);
                list-style: none;
                padding: 0 5px;


                a {
                    cursor: pointer;
                    text-decoration: none;
                }

                img {
                    max-width: 80px;
                    height: 80px;
                    cursor: pointer;
                }

                .title-menu {

                    padding: 0 10px;

                    a {
                        white-space: nowrap;
                        font-size: 0.9rem;
                        color: white;
                        text-transform: uppercase;
                    }

                }
            }
        }
    }
}
</style>