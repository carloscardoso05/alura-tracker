<template>
    <div class="box has-text-weight-bold" :style="estilos">
        <slot></slot>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    name: 'Box-name',
    data () {
        return {
            estilos: {
                backgroundColor: '#faf0ca',
                // 'background-color': '#faf0ca',
                // background: '#faf0ca'
            }
        }
    }
})
</script>

<!-- <style scoped>
.box {
    background-color: #faf0ca;
}
</style> -->