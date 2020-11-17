<template lang="pug">
.hero.w-full
  .hero__inner.container.mx-auto.flex.justify-end.relative
    .hero__content.absolute.w-full.flex.flex-col.items-center
      .hero__title.font-bold 「食の安全・安心」を支える
      .hero__desc.font-bold HACCP対応ユニフォーム
    .hero__wrap
      .hero__cover
      .hero__img
        img(src="~assets/header-image.jpg")
</template>
<script>
export default {
  methods: {
    slideCover(cover, img, text) {
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
      tm.to(cover, 1, { top: 0, bottom: "100%", ease: Power4.easeOut });
      tm.to(img, 1, { opacity: 1 }, "-=0.7");
      tm.to(text, 1, { opacity: 1, y: "-40px" }, "-=0.7");
    },
  },
  mounted() {
    this.slideCover(".hero__cover", ".hero__img img", ".hero__content");
  },
};
</script>
<style scoped lang="scss">
.hero {
  &__content {
    z-index: 2;
    top: 75%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0;
  }
  &__title {
    font-size: 1rem;
    color: #3d7df1;
    text-shadow: 2px 2px 10px #fff;
    @media screen and (min-width: 480px) {
      font-size: 2rem;
    }
    @media screen and (min-width: 1028px) {
      font-size: 4rem;
    }
  }
  &__desc {
    font-size: 0.5rem;
    text-shadow: 2px 2px 10px #fff;
    @media screen and (min-width: 480px) {
      font-size: 1rem;
    }
    @media screen and (min-width: 1028px) {
      font-size: 2.5rem;
    }
  }
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
