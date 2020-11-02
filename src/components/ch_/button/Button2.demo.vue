<demo>
样式按钮
</demo>
<template>
<div>
    <div>
        <Button size="big">大老头</Button>
        <Button>中年老头</Button>
        <Button size="small">小老头</Button>
    </div>
    <div>
        <Button theme="link" size="big">大老头</Button>
        <Button theme="link">中年老头</Button>
        <Button size="small" theme="link">小老头</Button>
    </div>
    <div>
        <Button size="big" theme="text">大老头</Button>
        <Button theme="text">中年老头</Button>
        <Button size="small" theme="text">小老头</Button>
    </div>
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
