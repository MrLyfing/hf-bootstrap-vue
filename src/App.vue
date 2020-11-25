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
        <b-col></b-col>
        <b-col>
          <b-card no-body class="m-4" bg-variant="dark" header="Buttons">
            <b-card-body class="text-center">
              <b-button
                v-for="(v, i) in variants"
                :key="i"
                :variant="v.toLowerCase()"
                class="m-3"
              >
                {{ v }}
              </b-button>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
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
