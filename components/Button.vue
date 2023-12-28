<template>
  <button
    @click.prevent="$emit('click')"
    class="border-all dim-white-border flex-center duration-2000 hover:gradient mx-auto min-h-10 w-fit min-w-10 flex-col gap-0.5 rounded p-1 shadow-md outline-none transition-all ease-in-out hover:shadow-lg"
    :style="`transform: scale(${scale / 100})`"
  >
    <img v-if="icon" :src="icon" alt="" />
    <span v-if="text" class="text-xs uppercase tracking-wider">
      {{ text }}
    </span>
  </button>
</template>
<script setup>
const props = defineProps({
  text: String,
  icon: String,
  scale: {
    type: Number,
    default: 100
  },
  isSuccess: {
    type: Boolean,
    default: false
  },
  isDanger: {
    type: Boolean,
    default: false
  }
})
</script>
