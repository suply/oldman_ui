<demo>
导航条
</demo>
<template>
<Tabs v-model:selected="x">
    <Tab title="导航1">任务1</Tab>
    <Tab title="导航2">任务2</Tab>
</Tabs>
</template>

<script lang="ts">
import {
    Tabs,
    Tab
} from "../../../lib/index";
import {
    ref
} from 'vue'
export default {
    components: {
        Tabs,
        Tab
    },
    setup() {
        const x = ref('导航2')
        return {
            x
        }
    }
}
</script>
