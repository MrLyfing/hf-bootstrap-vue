<template>
  <b-card class="m-4 text-center">
    <h3>
      <a href="https://bootstrap-vue.org/docs/components/button" target="_blank"
        >Buttons</a
      >
    </h3>
    <b-button
      v-for="(v, i) in variants"
      :key="i"
      :variant="v.toLowerCase()"
      class="m-3"
    >
      {{ v }}
    </b-button>
  </b-card>
</template>

<script>
export default {
  props: {
    variants: {type: Array, required: true},
  },
}
</script>
