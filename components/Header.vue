<template lang="pug">
header.header.w-full
  .header__inner.container.mx-auto.flex.justify-between.items-center
    h1.header__logo
      svgLogo
    nav.header__nav
      ul.header__ul.flex
        a(
          v-for="(category, index) in categorys",
          :key="index",
          :href="category.link"
        )
          li.header__li.ml-5.font-bold.text-sm {{ category.title }}
</template>
<script>
import svgLogo from "../assets/logo.svg";
export default {
  components: {
    svgLogo,
  },
  data() {
    return {
      categorys: [
        {
          title: "HOME",
          link: "http://www.daimaru-hakui.co.jp/index.html",
        },
        {
          title: "COMPANY",
          link: "http://www.daimaru-hakui.co.jp/company.html",
        },
        {
          title: "CONTACT",
          link: "http://www.daimaru-hakui.co.jp/contact.html",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
.header {
  &__inner {
    width: 100%;
    height: 70px;
    // @media screen and (min-width: 768px) {
    //   width: 1000px;
    // }
  }
}
svg {
  width: 200px;
}
</style>
