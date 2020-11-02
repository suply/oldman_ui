<template>
<h1>导航栏仓库</h1>
<Demo :component="Tabs1Demo" />
</template>

<script lang="ts">
import Demo from './Demo.vue'
import Tabs1Demo from './ch_/tabs/Tabs1.demo.vue'
export default {
    components: {
        Demo
    },
    setup() {
        return {
            Tabs1Demo
        }
    }
}
</script>
