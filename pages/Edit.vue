<template>
  <div id="edit_page" class="flex">
    <div class="edit__category grid grid-cols-1 grid-rows-10 items-center">
      <div
        class="edit__category-row flex active h-full items-center px-5"
        id="header"
      >
        <IconsSetting class="mx-2" />
        <p>Header</p>
      </div>
    </div>
    <div class="edit__content mx-5 flex flex-col">
      <div class="edit__text border-b-2 border-gray-800 pb-5">
        <h2 class="font-semibold text-xl px-5 text-red-400">Header</h2>
      </div>
      <div
        class="edit__tab-content flex-1 grid grid-cols-3 grid-rows-4 gap-3 p-3"
      >
        <div
          v-for="(header, index) in APICategory.headers"
          :key="'header' + index"
          class="
            edit__item
            border-2 border-gray-800
            rounded-xl
            overflow-hidden
            cursor-pointer
            flex flex-col
          "
          @click="handleSetHeader('header', index, 'header 1')"
        >
          <img
            :src="header.img"
            alt=""
            class="w-full h-auto flex-1 object-contain"
          />
        </div>
      </div>
    </div>
    <div
      class="
        edit__template
        fixed
        right-0
        top-0
        h-screen
        rounded-l-lg
        p-5
        flex flex-col
      "
    >
      <h5 class="font-semibold mb-5">Layout #34562</h5>
      <div
        class="
          edit__template-header
          flex-1
          border-dashed border-2 border-red-500
          p-3
        "
      >
        <div
          class="
            flex
            items-center
            justify-between
            border-2 border-gray-800
            rounded-lg
            p-2
          "
        >
          <div class="flex-1 text-gray-600 font-semibold">
            <p>* Header Type 1</p>
          </div>
          <div class="flex">
            <div class="icon-type1 mx-2">
              <IconsTrash class="absolute inset-0 m-auto" />
            </div>
          </div>
        </div>
      </div>
      <div
        class="
          mx-auto
          mt-3
          cursor-pointer
          shadow-xs
          border-2 border-red-500
          rounded-lg
          text-red-500
          hover:bg-red-500 hover:text-white
        "
      >
        <p class="p-3 rounded-lg">Tạo template mẫu</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    APICategory: {
      headers: [
        {
          id: 1,
          tag: 'header',
          name: 'header 1',
          img: '../assets/images/header/Screenshot_3.jpg',
          htmlCode: '',
          cssCode: '',
          jsCode: '',
        },
        {
          id: 2,
          tag: 'header',
          name: 'header 1',
          img: '../assets/images/header/Screenshot_3.jpg',
        },
        {
          id: 3,
          tag: 'header',
          name: 'header 1',
          img: '../assets/images/header/Screenshot_3.jpg',
        },
        {
          id: 4,
          tag: 'header',
          name: 'header 1',
          img: '../assets/images/header/Screenshot_3.jpg',
        },
        {
          id: 5,
          tag: 'header',
          name: 'header 1',
          img: '../assets/images/header/Screenshot_3.jpg',
        },
      ],
    },

    templateDemo: {
      header: {},
    },

    codeFinal: {},
  }),

  methods: {
    handleSetHeader(tagComponent, idComponent) {
      // API get Info Header
      // eslint-disable-next-line no-console
      console.log(tagComponent + idComponent)
      this.templateDemo.header = {
        name: '',
        htmlCode: '<h1>adasdasdasds</h1>',
        cssCode: '.helo{}',
        jsCode: '<ádscript></áscript>',
      }
      // eslint-disable-next-line no-console
      console.log(this.templateDemo)
    },
  },
}
</script>

<style lang="scss" scoped>
.edit {
  &__category {
    width: 275px;
    height: 723px;
    background-color: #1f1d2b;
    border-radius: 10px;
    padding: 24px 0;

    &-row {
      fill: white;
      cursor: pointer;

      &.active {
        background-color: #54353b;
        fill: #ea7c69;
        color: #ea7c69;
      }
    }
  }

  &__content {
    width: 743px;
    min-height: 723px;
    background-color: #1f1d2b;
    border-radius: 10px;
    padding: 24px 0;
  }

  &__template {
    width: 409px;
    background-color: #1f1d2b;
  }
}

.icon-type1 {
  @apply rounded-lg border-2 border-white w-10 h-10 relative cursor-pointer;
  fill: white;

  &:hover {
    @apply border-red-500;
    fill: #f56565;
  }
}

.grid-rows-10 {
  grid-template-rows: repeat(10, minmax(0, 1fr));
}
</style>
