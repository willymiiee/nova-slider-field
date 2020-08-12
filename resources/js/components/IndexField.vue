<template>
    <vue-slider ref="slider" v-model="field.value"
                :tooltip="field.tooltip || 'false'"
                disabled
                :disabled-style="{cursor: 'default', opacity: 1}"
                :min="field.min || 0"
                :max="field.max || 100"
                :interval="field.interval || 1">
    </vue-slider>
</template>

<script>
import vueSlider from 'vue-slider-component'
export default {
    components: {
        vueSlider,
    },
    props: ['resourceName', 'field'],
}
</script>
