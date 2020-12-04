<template>
  <div class="d-flex flex-column min-vh-100">
    <b-container fluid class="flex-grow-1 py-3">
      <b-row>
        <b-col class="text-center">
          <b-dropdown text="Theme">
            <b-dd-item-btn
              v-for="(t, i) in theme.options"
              :key="i"
              :active="t === theme.selected"
              @click="switchTheme(t)"
            >
              {{ t }}
            </b-dd-item-btn>
          </b-dropdown>
        </b-col>
      </b-row>

      <b-row>
        <b-col lg></b-col>
        <b-col lg>
          <Buttons :variants="variants" />
        </b-col>
      </b-row>
      <b-row>
        <b-col lg></b-col>
        <b-col lg>
          <Tooltips />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Buttons from './cards/Buttons.vue'
import Tooltips from './cards/Tooltips.vue'

export default {
  components: {
    Buttons,
    Tooltips,
  },

  data() {
    var themes = ['default', 'black', 'gray', 'white'].map((t) => 'theme-' + t)
    document.body.className = themes[0]

    return {
      theme: {
        selected: themes[0],
        options: themes,
      },
      variants: [
        'Primary',
        'Secondary',
        'Success',
        'Danger',
        'Warning',
        'Info',
        'Light',
        'Dark',
      ],
    }
  },
  methods: {
    switchTheme(theme) {
      this.theme.selected = theme
      document.body.className = theme
    },
  },
}
</script>
