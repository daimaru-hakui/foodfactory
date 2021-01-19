<template lang="pug">
div
  Header
  .content.mt-24
    .content__inner.mx-auto.px-1
      .content__image.w-full
        img(src="~assets/SP2002.jpg")
      .content__box.w-full
        h1.number-name.mt-10.text-3xl SP2002 男女兼用ブルゾン（長袖）
        .price.text-2xl.mt-2 ￥4,800
          span.text-xs +税
        .material.text-xs 素材：ポプリン（ポリエステル65%/綿35%）
        .content__option.flex.mt-5.text-xs
          .content__label 男女兼用
          .content__label 制電
          .content__label 体毛落下防止
          .content__label 工業洗濯
        table.content__size.w-full.mt-10.text-center.text-sm
          tr
            th サイズ
            td S
            td M
            td L
            td LL
            td 3L
            td 4L
            td 5L
          tr
            th バスト
            td 105
            td 111
            td 118
            td 126
            td 135
            td 145
            td 156
          tr
            th 着丈
            td 64
            td 67
            td 70
            td 73
            td 76
            td 76
            td 79
          tr
            th 裄丈（フライス含）
            td 72
            td 76
            td 80
            td 82
            td 84
            td 84
            td 84
  .product.mt-24
    .product__inner.mx-auto.px-1
      h2.product__explain.text-center.py-1.text-white 商品説明
      .product__detail
        h3.product__title.flex.flex-col.text-2xl.mt-16.mb-16.text-center タイトルタイトルタイトルタイトル
          span タイトルタイトル
      p.mx-auto.text-sm 上質感と機能性が人気のurban techシリーズと同素材を採用し、クラシコ品質はそのままに装飾などを最低限に削ぎ落とすことでこれまでにない圧倒的な低価格を実現しました。低価格ながらも、シンプル、スタイリッシュ、上質というクラシコの世界観に恥じない仕上がりの白衣です。
  Contact
  Footer
</template>
<style scoped lang="scss">
.content {
  &__inner {
    width: 100%;
    @media screen and (min-width: 768px) {
      width: 1000px;
    }
  }
  &__label {
    margin-right: 5px;
    padding: 2px 5px;
    color: white;
    border: 1px solid black;
    background-color: black;
  }
  &__size tr {
    border-top: 1px solid #a0aec0;
  }
  &__size th {
    min-width: 100px;
    border-bottom: 1px solid #a0aec0;
  }
  &__size td {
    min-width: 40px;
    border-bottom: 1px solid #a0aec0;
  }
}
.product {
  &__inner {
    width: 100%;
    @media screen and (min-width: 768px) {
      width: 1000px;
    }
  }
  &__explain {
    background-color: #a0aec0;
  }
  &__title {
    position: relative;
  }
  &__title::before {
    content: "";
    position: absolute;
    background-color: black;
    bottom: -15px;
    left: 50%;
    height: 1px;
    width: 100px;
    transform: translateX(-50%);
  }
  & p {
    max-width: 700px;
  }
}
</style>

