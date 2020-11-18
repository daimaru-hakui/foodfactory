<template lang="pug">
.title.mt-20
  .title__inner.container.mx-auto.flex.flex-col.text-center.font-bold.text-black
    .title__en.text-3xl
      <slot name="title-en" />
    .title_ja.text-3xl
      <slot name="title-ja" />
</template>
<style scoped lang="scss">
.title {
  margin: 5rem 0 2rem;
}
</style>
