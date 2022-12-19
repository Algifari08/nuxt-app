<template>
  <div>
    <Card title="Image" image="https://www.usetada.com/wp-content/uploads/2022/11/Extensively-integrated-Retailer-Integration.webp" />
    <ButtonApp />
  </div>
</template>

<script>
import ButtonApp from '~/components/Form/ButtonApp'

export default {
  name: 'IndexPages',
  components: {
    ButtonApp,
  },
  layout: 'test-layout',
  created() { 
    this.getBanner()
  },
  data() { 
    return {
      banners: null,
    }
  },
  methods: {
    getBanner() { 
      // API
      const data = [
          {
            nama: 'Test',
            title: 'Desc'
          }
      ]

      this.banners = data
    }
  }
}
</script>
