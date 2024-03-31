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
    width: 100%;
    height: 16px;

    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;

    &__link {
        margin-right: 4px;
        text-decoration: none;
        color: #828EAD;

        &:not(:first-child)::before {
            content: '/';
            line-height: 16px;
            font-size: 12px;
            font-weight: 400;
            margin-right: 4px;
        }
    }
}
</style>
