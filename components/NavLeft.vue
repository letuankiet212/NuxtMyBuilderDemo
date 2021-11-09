<template>
  <div
    class="navleft rounded-r-xl grid grid-cols-1 grid-rows-6 py-10 items-center"
  >
    <div class="navleft__link">
      <IconsHome
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
    <div class="navleft__link active">
      <IconsEdit
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
    <div class="navleft__link">
      <IconsRestaurant
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
    <div class="navleft__link">
      <IconsSetting
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
    <div class="navleft__link">
      <IconsDownload
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
    <div class="navleft__link">
      <IconsLogout
        class="navleft__icon absolute w-6 h-6 m-auto inset-0 icon-color"
      />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.navleft {
  background-color: #1f1d2b;
  width: 104px;
  height: 100%;
  min-height: 100vh;
  position: fixed;

  &__link {
    width: 56px;
    height: 56px;
    @apply my-2 relative mx-auto transition-colors duration-300 cursor-pointer rounded-lg;

    &:hover,
    &.active {
      box-shadow: 1px 1px 10px #f56565;
      background-color: #f56565;

      &:before {
        content: '';
        position: absolute;
        top: 0;
        bottom: 0;
        margin: auto 0;
        left: -12px;
        background-image: url('~/assets/images/navleft/pattern.png');
        background-position: center right;
        background-repeat: no-repeat;
        width: 93px;
        height: 105px;
        z-index: -1;
      }
    }
    &:hover .navleft__icon,
    &.active .navleft__icon {
      fill: white !important;
    }
  }

  &__icon {
    fill: #ea7c69;
  }
}
.icon-color {
}
</style>
