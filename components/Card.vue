<!-- Please remove this file from your project -->
<template>
  <div class="card">
    <div class="card-body">
      <img :src="image" alt="">
      <div class="row">
        <div class="col-sm-12">
          {{ title }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    title: String,
    image: String,
  }
}
</script>

