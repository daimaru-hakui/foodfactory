<template lang="pug">
.hero.w-full.mt-5
  .hero__inner.container.mx-auto.flex.justify-end
    //- .hero__content
    //-   .hero__title
    //-   .hero__disc
    .hero__wrap
      .hero__cover
      .hero__img
        img(src="~assets/foodfactory.jpg")
</template>
<script>
export default {
  methods: {
    slideCover(cover, img) {
      let tm = new TimelineMax({
        scrollTringger: {
          trigger: img,
          start: "top top",
        },
      });
      tm.to(cover, 1, {
        delay: 1,
        top: 0,
        bottom: 0,
        ease: Power4.easeOut,
      });
      tm.to(cover, 0.7, { top: 0, bottom: "100%", ease: Power4.easeOut });
      tm.to(img, 0.7, { opacity: 1 }, "-=0.5");
    },
  },
  mounted() {
    this.slideCover(".hero__cover", ".hero__img img");
  },
};
</script>
<style scoped lang="scss">
.hero {
  &__wrap {
    position: relative;
  }
  &__cover {
    position: absolute;
    width: 100%;
    top: 100%;
    bottom: 0;
    background-color: #2979dc;
    z-index: 1;
  }
  & img {
    opacity: 0;
  }
}
</style>
