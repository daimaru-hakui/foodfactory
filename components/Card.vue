<template lang="pug">
section.card-area.w-full.mt-2
  .card-area__inner.container.mx-auto.flex.flex-wrap
    .card.w-full.mb-4(
      class="sm:w-1/3 lg:w-1/5",
      v-for="(item, index) in items",
      :key="index"
    )
      .card__inner.mx-2.p-4.relative
        .card__number.absolute.flex.items-center.justify-center {{ index + 1 }}
        .card__textbox.text-center
          .card__title.text-base.font-bold.mb-2 {{ item.title }}
          .card__desc.text-sm.mb-2 {{ item.desc }}
        //- figure.card__img
        //-   img(src="~/assets/card_01.jpg")
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: "コストパフォーマンス",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "暑さ対策",
          desc: "テキストテキストテキスト",
        },
        {
          title: "防寒対策",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "エコマーク",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "抗ウィルス",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
      ],
    };
  },
};
</script>
<style scoped lang="scss">
.card {
  &__inner {
    height: 100%;
    border-bottom: 1px solid #202063;
    background-color: #d9dde0;
  }
  &__number {
    top: 0;
    left: 50%;
    width: 80px;
    height: 80px;
    transform: translate(-50%, 0);
    color: white;
    font-size: 2rem;
    background-color: #202063;
  }
  &__textbox {
    margin-top: 80px;
  }
}
</style>
