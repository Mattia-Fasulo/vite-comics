<template>
    <div class="footer-bot">
        <div class="container">
            <div class="footer-btn">
                <button>Sign-Up Now</button>
            </div>
            <div class="footer-social">
                <h3>Fallow Us</h3>
                <ul>
                    <li v-for="(social, index) in links" :key="index">
                        <a :href="social.url">
                            <img :src="social.img" :alt="social.title">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import { socials } from '../data/links'
export default {
    name: 'FooterBottom',
    data() {
        return {
            links: socials,
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.footer-bot {
    position: relative;
    z-index: 100;
    height: 120px;
    background-color: $light-black;

    .container {
        @include center('horizontal');
        justify-content: space-between;
        height: 100%;
    }
}

.footer-btn {

    button {
        cursor: pointer;
        padding: 10px;
        text-transform: uppercase;
        font-weight: 700;
        color: white;
        background-color: $light-black;
        border-color: $blu;
    }
}

.footer-social {
    @include center();

    ul {
        @include center();

        li {
            list-style: none;
            margin: 0 10px;
        }
    }

    h3 {
        margin-right: 10px;
        cursor: pointer;
        color: $blu;
        text-transform: uppercase;
    }
}
</style>