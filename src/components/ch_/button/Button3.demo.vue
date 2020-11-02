<demo>
颜色按钮
</demo>
<template>
<div>
    <div>
        <Button level="main">老头</Button>
    </div>
    <div>
        <Button theme="text">普通老头</Button>
    </div>
    <div>
        <Button theme="text" level="main">有学识的老头</Button>
        <Button theme="text">普通老头</Button>
        <Button theme="text" level="danger">危险的老头</Button>
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
