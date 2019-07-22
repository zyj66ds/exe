<template>
  <div>
    <p>Original message:"{{ message }}"</p>
    <p>Computed reversed message:(用computed写的) "{{ reversedMessage }}"</p>
  </div>
</template>
<script>
export default {
  data () {
    return {
      message: 'Hello'
    }
  },
  props: [] || { author: 'zyj' },
  components: {},
  filters: {},
  computed: {
    reversedMessage: function () {
      return this.message
        .split('')
        .reverse()
        .join('')
    }
  },
  watch: {},
  beforeCreate () {},
  created () {},
  beforeMount () {},
  mounted () {},
  beforeUpdate () {},
  updated () {},
  beforeDestroy () {},
  destroyed () {},
  methods: {
    ForDight (Dight, How) {
      Dight = Math.round(Dight * Math.pow(10, How)) / Math.pow(10, How)
      return Dight
    }
  }
}
</script>
