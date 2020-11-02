<template>
<div class="layout">
    <Topnav togMenButtonVisible class="nav" />
    <div class="content">
        <aside v-if="menuVisible">
            <h3>文档</h3>
            <ol>
                <li>
                    <router-link to="/doc/intro">介绍</router-link>
                </li>
                <li>
                    <router-link to="/doc/install">安装</router-link>
                </li>
                <li>
                    <router-link to="/doc/get-started">开始</router-link>
                </li>
            </ol>
            <h3>老头的任务库</h3>
            <ol>
                <li>
                    <router-link to="/doc/button">按钮</router-link>
                </li>
                <li>
                    <router-link to="/doc/dialog">弹窗</router-link>
                </li>
                <li>
                    <router-link to="/doc/tabs">导航栏(创建中...)</router-link>
                </li>
                <li>
                    <router-link to="/doc/switch">开关(创建中...)</router-link>
                </li>
            </ol>
        </aside>
        <main>
            <router-view />
        </main>
    </div>
</div>
</template>

<script lang="ts">
import Topnav from "../components/Topnav.vue";
import {
    inject,
    Ref
} from "vue";
export default {
    components: {
        Topnav
    },
    setup() {
        const menuVisible = inject < Ref < boolean >> ("menuVisible"); // get
        return {
            menuVisible
        };
    },
};
</script>

<style lang="scss" scoped>
.layout {
    z-index: 99;
    display: flex;
    flex-direction: column;
    height: 100vh;

    >.nav {
        flex-shrink: 0;
    }

    >.content {
        flex-grow: 1;
        padding-top: 100px;
        padding-left: 156px;

        @media (max-width: 500px) {
            padding-left: 0;
        }
    }
}

.content {
    display: flex;

    >aside {
        flex-shrink: 0;
    }

    >main {
        flex-grow: 1;
        padding: 16px;
        background: white;
    }
}

aside {
    background: rgb(235 248 250);
    width: 150px;
    padding: 16px 15px;
    position: fixed;
    top: 0;
    left: 0;
    padding-top: 100px;
    height: 100%;

    >h2 {
        margin-bottom: 4px;
        padding: 4px 10px;
    }

    >ol {
        >li {
            >a {
                display: block;
                padding: 4px 10px;
                border-radius: -20px;
            }

            .router-link-active {
                background: rgb(182 206 210);
                border-radius: 5px
            }

            padding:6px 0px;
        }
    }
}

main {
    overflow: auto;
}
</style>
