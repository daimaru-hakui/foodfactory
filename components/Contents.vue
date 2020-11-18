<template lang="pug">
section.contents.mb-10
  .contents__inner.mx-auto.mt-20.flex.flex-col.w-full(class="md:flex-row")
    .contents__boxtext.w-full.p-5(class="md:w-3/6")
      .contents__title.mb-5.font-bold.text-3xl HACCPについて
      .contents__text.text-sm.leading-6.tracking-wider(v-html="haccpText") 
      span.contents__button.mt-4.py-2.px-5.inline-block ⇒ READ MORE
    .contents__image.m-5(class="md:w-3/6")
      img.rounded-xl(src="../assets/haccp.jpg")
</template>
<script>
export default {
  data() {
    return {
      haccpText:
        "我々の食の安全を守るための法律、食品衛生法が2018年6月に改正。<br>2020年から施工され、１年の経過措置を経て2021年6月から食品等事業者を対象にHACCPによる衛生管理が義務化されることになりました。<br>これにより事業規模に関わらず食品製造業者はHACCPに沿った衛生管理に取り組んでいく必要がありますが、そもそもHACCPとは一体どのようなものなのでしょうか？<br>ここではHACCPについての基礎知識からHACCPの取り組み方、そしてユニフォームによるHACCP対策など、弊社が収集した情報や知識などをご紹介致します。<br>是非、貴社のHACCP対策にお役立てください。",
    };
  },
};
</script>
<style scoped lang="scss">
.contents {
  &__inner {
    width: 100%;
    @media screen and (min-width: 768px) {
      width: 1100px;
    }
  }
  &__button {
    background-color: #eee;
  }
}
</style>
