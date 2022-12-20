<!-- Please remove this file from your project -->
<template lang="pug">
a.btn.btn-primary.btn-lg(v-if="type === 'submit'" :type="`${type}`") {{ title }}
a.btn.btn-primary.btn-lg(v-else-if="type === 'link'" :href="`${link}`") {{ title }}
</template>

<script>
export default {
  name: 'ButtonApp',
  props: {
    title: String,
    type: String,
    link: String
  }
}
</script>

