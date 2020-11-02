<demo>
常规使用
</demo>
<template>
<div>
    <Button @click="toggle">获取老头的任务</Button>
    <Dialog v-model:visible="x" :closeOnClickOverlay="false" :ok="f1" :cancel="f2">
        <template v-slot:content>
            <strong>任务1：上厕所</strong>
            <div>女装上厕所</div>
            <strong>任务2：下厕所</strong>
            <div>女装下厕所</div>
        </template>
        <template v-slot:title>
            <strong>女装</strong>
        </template>
    </Dialog>
</div>
</template>

<script lang="ts">
import {
    Button,
    Dialog
} from "../../../lib/index"
import {
    ref
} from 'vue'
import {
    openDialog
} from '../../../lib/openDialog'
export default {
    components: {
        Dialog,
        Button
    },
    setup() {
        const x = ref(false)
        const toggle = () => {
            x.value = !x.value
        }
        const f1 = () => {
            return false
        }
        const f2 = () => {}
        return {
            x,
            toggle,
            f1,
            f2
        }
    }
}
</script>
