<template lang="pug">
section.card-area.w-full.mt-5
  .card-area__inner.container.mx-auto.flex.flex-wrap
    .card(class="w-1/3", v-for="(item, index) in items", :key="index")
      .card__inner.mx-2.mb-4.p-4
        .card__textbox
          .card__title.text-xl.mb-2 {{ item.title }}
          .card__desc.text-sm.mb-2 {{ item.desc }}
        figure.card__img
          img(src="~/assets/card_01.jpg")
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: "タイトル1",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "タイトル2",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "タイトル3",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "タイトル4",
          desc:
            "テキストテキストテキストテキストテキストテキストテキストテキスト",
        },
        {
          title: "タイトル5",
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
    background-color: #d7eefe;
  }
}
</style>
