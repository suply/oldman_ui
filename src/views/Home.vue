<template>
<div>
    <div class="topAndBottom">
        <Topnav />
        <div class="banner">
            <h1>oldMan UI</h1>
            <h3>老头UI，一套基于 Vue 3.0 的桌面端组件库，助你快速完成老头的任务。</h3>
            <p class="actions">
                <a href="https://github.com/suply/supply-ui">GitHub</a>
                <router-link to="/doc">开始</router-link>
            </p>
        </div>
    </div>
    <div class="adv">
        <div>
            <svg class="icon">
                <use xlink:href="#icon-Vues"></use>
            </svg>
            <div class="adv_a">
                <h3>基于VUE3</h3>
                <p>使用vue 3.0开发</p>
            </div>

        </div>
        <div>
            <svg class="icon">
                <use xlink:href="#icon-TS"></use>

            </svg>
            <div class="adv_a">
                <h3>基于TS</h3>
                <p>采用TypeScript源码</p>
            </div>
        </div>
        <div>
            <svg class="icon">
                <use xlink:href="#icon-ic-easy"></use>

            </svg>
            <div class="adv_a">
                <h3>简化开发</h3>
                <p>代码简洁,引用便利安全</p>
            </div>
        </div>
    </div>
</div>
</template>

<script lang="ts">
import Topnav from "../components/Topnav.vue";
export default {
    components: {
        Topnav
    },
};
</script>

<style lang="scss" scoped>
.adv {
    @media (max-width: 500px) {
        display: flex;
        flex-direction: column;
    }

    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin:0 70px;

    >div {
        display: flex;
        flex-direction: row;

        >.adv_a {
            margin-top: 20px;

            >p {
                font-size: 14px;
            }
        }

        >svg {

            width: 64px;
            height: 80px;
        }
    }

}

.topAndBottom {
    background: rgb(255, 255, 255);
    background: linear-gradient(149deg, rgba(255, 255, 255, 1) 0%, rgba(58, 109, 124, 1) 100%);
    clip-path: ellipse(80% 60% at 60% 40%);
}

.banner {
    color: rgb(1 67 97);
    padding: 100px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 500px;

    >.actions {
        padding: 8px 0;

        a {
            margin: 0 16px;
            background: #0089b0;
            color: #fff;
            padding: 5px 20px;
            border-radius: 8px;
            display: inline-block;

            a:hover {
                text-decoration: none;
            }

        }
    }
}
</style>
