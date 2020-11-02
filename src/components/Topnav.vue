<template>
<div class="topnav">
    <router-link to="/" class="logo">
        <svg class="icon">
            <use xlink:href="#icon-oldman"></use>
        </svg>
    </router-link>
    <ul class="menu">
        <router-link to="/doc">文档</router-link>
        <router-link to="/sh">支持</router-link>
    </ul>
    <svg v-if="togMenButtonVisible" class="toggleAside" @click="toggleMenu">
        <use xlink:href="#icon-home"></use>
    </svg>
</div>
</template>

<script lang="ts">
import {
    inject,
    Ref
} from "vue";
export default {
    props: {
        togMenButtonVisible: {
            type: Boolean,
            default: false
        }
    },
    setup() {
        const menuVisible = inject < Ref < boolean >> ("menuVisible"); // get
        const toggleMenu = () => {
            menuVisible.value = !menuVisible.value;
        };
        return {
            toggleMenu
        };
    },
};
</script>

<style lang="scss" scoped>
.topnav {

    >.logo {
        max-width: 6em;
        margin-right: auto;

        >svg {
            width: 40px;
            height: 40px;
        }
    }

    background-color: rgb(224 248 255);
    display: flex;
    padding: 16px;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 100;
    justify-content: center;
    align-items: center;
    box-shadow: 0px 20px 20px -20px #5E5E5E;

    >.menu {
        display: flex;
        white-space: nowrap;
        flex-wrap: nowrap;

        >a {
            margin: 0 8px;
        }
    }

    >.toggleAside {
        width: 24px;
        height: 24px;
        position: absolute;
        left: 16px;
        top: 50%;
        transform: translateY(-50%);
        display: none;
    }

    @media (max-width: 500px) {
        >.menu {
            display: none;
        }

        >.logo {
            margin: 0 auto;

            >svg {
                width: 40px;
                height: 40px;
            }
        }

        >.toggleAside {
            display: inline-block;
        }
    }
}
</style>
