<template lang="pug"> 
.banner 
  .banner__container
    .banner__wrapper
      .banner__txt
        h2.banner__title {{ bannerTitle }}
        p.article__desc {{ bannerDesc }}
      .banner__form
        form.banner__fi(action="POST")
          ='\n'
          input.banner__input(type="text")/
          ='\n'
        ButtonApp(
          title="Get Free trial"
          type="link"
          link="/product"
        )
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
      bannerTitle: 'The Best Software to Grow your Sales and Services',
      bannerDesc: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat',
      classApp: 'container-fluid mt-5 mb-2 ml-2 mr-5'
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

<style lang="scss">

</style>
