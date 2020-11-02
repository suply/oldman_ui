<template>
<h1>弹窗库</h1>
<Demo :component="Dialog1Demo" />
<Demo :component="Dialog2Demo" />
</template>

<script lang="ts">
import Demo from './Demo.vue';
import Dialog1Demo from './ch_/dialog/Dialog1.demo.vue';
import Dialog2Demo from './ch_/dialog/Dialog2.demo.vue';
export default {
    components: {
        Demo
    },
    setup() {
        return {
            Dialog1Demo,
            Dialog2Demo
        }
    }
}
</script>
