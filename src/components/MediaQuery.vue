<script>
export default {
  name: 'mediaQuery',
  props: {
    at: {
      type: [String, Number]
    },
    maxWidth: {
      type: Boolean,
      default: false
    },
    minWidth: {
      type: Boolean,
      default: false
    },
    unit: {
      type: String,
      default: 'px',
      validator: value => ['px', '%'].includes(value)
    }
  },
  mounted () {
    window.addEventListener('resize', this.onResize)
    this.onResize()
  },
  beforeDestroy () {
    window.removeEventListener('resize', this.onResize)
  },
  methods: {
    onResize () {
      // todo
    }
  },
  render () {
    if (this.maxWidth && this.minWidth) {
      console.warn(`The props 'max-width' and 'min-width' are active when only one is allowed.`)
      return
    }

    return this.$slots.default[0]
  }
}
</script>
