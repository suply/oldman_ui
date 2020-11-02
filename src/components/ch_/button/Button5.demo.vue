<demo>
加载按钮
</demo>
<template>
<div>
    <Button loading>老头任务加载中...</Button>
    <Button>老头任务加载完毕</Button>
</div>
</template>

<script lang="ts">
import {
    Button
} from "../../../lib/index";
export default {
    components: {
        Button
    }
}
</script>
