<script setup lang="ts">
const breadcrumbs = [{ id: 1, title: 'Каталог', link: '/1' }, { id: 2, title: 'Обувь', link: '/2' }, { id: 3, title: 'Кроссовки', link: '/3' }, { id: 4, title: 'Беговые', link: '/4' }]
</script>

<template>
  <div class="breadcrumbs">
    <a v-for="item in breadcrumbs" :key="item.id" class="breadcrumbs__link" :href="item.link">{{ item.title }}</a>
  </div>
</template>

<style scoped lang="scss">
.breadcrumbs {
  align-items: center;
  display: flex;
  gap: 4px;

  &__link {
    color: #828EAD;
    font-size: 12px;
    font-weight: 400;
    line-height: 16px;
    text-decoration: none;
    transition: opacity .3s;

    &:not(:last-child) {
      &:after {
        content: '/';
        margin-left: 4px;
      }
    }

    @media (hover: none), (pointer: coarse) {
      &:active {
        opacity: .7;
      }
    }

    @media not all and (pointer: coarse) {
      &:hover,
      &:active {
        opacity: .7;
      }
    }
  }
}
</style>
