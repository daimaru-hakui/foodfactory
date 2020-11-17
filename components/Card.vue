<template lang="pug">
section.card-area.w-full.mt-2
  .card-area__inner.container.mx-auto.flex.flex-wrap.justify-center
    .card.w-full.mb-4(
      class="sm:w-1/3 lg:w-1/3",
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
            "制電、体毛落下防止などの基本機能を備えたコストパフォーマンスモデル。標準的なポリエステル65%・綿35%と洗濯耐久性とイージーケアに優れたポリエステル100%の2タイプをご用意。",
        },
        {
          title: "暑さ対策",
          desc:
            "特殊生地を使用した高温作業用モデル。生地裏面の凹凸の点タッチ構造により、汗のベタつきを軽減できる「アクアクール」と、接触冷感と吸汗速乾姓を備えた機能素材「アイスフレッシュ」を使用した2タイプをご用意。",
        },
        {
          title: "防寒対策",
          desc:
            "冷蔵・冷凍などの寒い現場に最適な中綿入り防寒タイプ。暖かいのはもちろん、制電・体毛落下防止・ポケットなしのHACCP対応の食品工場向けの仕様です。",
        },
        {
          title: "エコマーク",
          desc:
            "環境意識の高いお客様に最適なエコ素材を使用したモデル。社会的に地球環境への関心が高まる中、環境意識の高さを消費者へアピールすることができます。",
        },
        {
          title: "抗ウィルス",
          desc:
            "全世界で流行のコロナウィルスを含む繊維上の特定のウイルスの数を99%減少させ、特定の細菌の増殖を抑制することができる抗ウィルス・抗菌タイプの食品工場向け白衣。",
          // 原料には安全性の高い口腔衛生用抗菌剤をベースにした、「Etak 」を使用しているので、人体や環境にも優しい素材です。",
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

