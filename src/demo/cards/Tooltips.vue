<template>
  <b-card class="m-4 text-center">
    <h3>
      <a
        href="https://bootstrap-vue.org/docs/components/tooltip"
        target="_blank"
        >Tooltips</a
      >
    </h3>
    <b-row class="text-center">
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.top="'Tooltip!'">Top</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.right="'Tooltip!'">Right</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.left="'Tooltip!'">Left</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.bottom="'Tooltip!'">Bottom</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.topright="'Tooltip!'">Top right</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.topleft="'Tooltip!'">Top left</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.bottomright="'Tooltip!'">Bottom right</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.bottomleft="'Tooltip!'">Bottom left</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.lefttop="'Tooltip!'">Left top</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.leftbottom="'Tooltip!'">Left bottom</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.righttop="'Tooltip!'">Right top</b-button>
      </b-col>
      <b-col cols="6" md="3" class="py-3">
        <b-button v-b-tooltip.rightbottom="'Tooltip!'">Right bottom</b-button>
      </b-col>
    </b-row>
  </b-card>
</template>
