<script setup lang="ts">

interface ExampleProps {
  message: string
}

const props = defineProps<ExampleProps>()
console.log("Message example: " + props.message)

</script>

<template>
  <p class="text-pink-500">Example Vue Component message: '{{ message }}'</p>
</template>
