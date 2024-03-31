<template>
  <a class="logo" href="javascript:void(0);" title="">
    <img alt="" height="" src="/public/logo.svg" width="">
  </a>
</template>

<style scoped lang="scss">
.logo {
  display: block;
  /* flex: none; */
  height: 48px;
  transition: opacity .3s;
  width: 144px;

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

  img {
    height: 100%;
    object-fit: contain;
    width: 100%;
  }
}
</style>
