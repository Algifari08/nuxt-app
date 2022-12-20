<!-- Please remove this file from your project -->
<template lang="pug">
.header
  .container-fluid.mx-3
    .header__wrapper 
      ='\n'
      a.header__logo(href="#")
        ='\n'
        img.header__logo__el(:src="`${logo}`" :alt="`${altLogo}`")/
        ='\n'
      ul.header__nav
          li(v-for="(item, index) in menus" :key="index").header__item 
            ='\n'
            a.header__link(:href="item.route")
              | {{ item.name }}
            ='\n'
      a.btn-primary {{ titleBtn }}
</template>

<script>
export default {
  name: 'Header',
  data() { 
    return {
      titleBtn: 'Free Trial',
      logo: null,
      altLogo: 'Header Logo',
      menus: [
        {
          name: 'Home',
          route: '/home'
        },
        {
          name: 'Product',
          route: '/product'
        },
        {
          name: 'Home',
          route: '/home'
        },
      ]
    }
  },
  created() { 
    this.getMenus()
    this.getLogo()
  },
  methods: {
    getMenus() { 
      const response = [
        {
          name: 'Home',
          route: '/home'
        },
        {
          name: 'Product',
          route: '/product'
        },
        {
          name: 'Pricing',
          route: '/pricing'
        },
        {
          name: 'About Us',
          route: '/about'
        },
        {
          name: 'Blog',
          route: '/blog'
        },
        {
          name: 'Contact',
          route: '/contact'
        }
      ]

      this.menus = response
    },
    getLogo() { 
      const response = '/img/logo/header-logo.svg'
      this.logo = response
    },
    nextHref(route) { 
      this.$router.push(route)
    }
  }
}
</script>


<style lang="scss">

</style>