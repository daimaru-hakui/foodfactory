<template lang="pug">
section.contact.w-full.mt-20
  .contact__inner.container.mx-auto.p-20.text-center.text-white
    .contact__title.text-3xl お問い合わせ
    .contact__desc.text-sm ご相談・ご質問等ございましたら、お気軽にお問い合わせください。
    .contact__box.flex.flex-col.mt-10(class="md:flex-row")
      .contact__item.contact__tel.flex.items-center.justify-center.text-2xl.text-center(
        class="md:w-1/2"
      ) tel：
        span.ml-1.text-4xl 06-6632-0891
      a.contact__item.contact__button.flex.items-center.justify-center.text-center.font-bold(
        class="md:w-1/2",
        href="http://www.daimaru-hakui.co.jp/contact.html"
      ) お問い合わせフォーム
</template>
<style scoped lang="scss">
.contact {
  background-color: #639eda;
  &__box {
    @media screen and (min-width: 768px) {
      padding: 0 100px;
    }
  }
  &__item {
    height: 80px;
  }
  &__tel {
    @media screen and (min-width: 768px) {
      border: 1px solid #ffffff;
    }
  }
  &__button {
    color: #639eda;
    border: 1px solid #ffffff;
    background-color: white;
    @media screen and (min-width: 768px) {
      border-left: none;
    }
  }
}
</style>