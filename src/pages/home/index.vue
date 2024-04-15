<template>
  <div class="back-btn-wrap"></div>
</template>
<script lang="ts" setup>
interface propsType {
  modelValue: string
}

const props = withDefaults(defineProps<propsType>(), {
  modelValue: ''
})

const emit = defineEmits(['update:modelValue'])
let InternalValue = computed({
  get: () => {
    return props.modelValue
  },

  set: (value: string) => {
    emit('update:modelValue', value)
  }
})
</script>
<style lang="scss" scoped>
.back-btn-wrap {
}
</style>
