<template>
    <panel-item :field="field">
        <template slot="value">
            <div class="flex items-center flex-wrap h-4">
                <div class="w-1/3">
                    <vue-slider ref="slider" v-model="field.value"
                                :tooltip="field.tooltip || 'false'"
                                disabled
                                :disabled-style="{cursor: 'default', opacity: 1}"
                                :min="field.min || 0"
                                :max="field.max || 100"
                                :interval="field.interval || 1">
                    </vue-slider>
                </div>
            </div>
        </template>
    </panel-item>
</template>

<script>
import vueSlider from 'vue-slider-component'
export default {
    components: {
        vueSlider,
    },
    props: ['resource', 'resourceName', 'resourceId', 'field'],
}
</script>
