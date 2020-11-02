<demo>
禁用按钮
</demo>
<template>
<Button disabled>无用老头</Button>
<Button theme="link" disabled>禁用老头</Button>
<Button theme="text" level="danger" disabled>点击老头无用</Button>
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
