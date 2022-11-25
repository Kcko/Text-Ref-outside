<template>
  <slot v-bind="{ textRef }" />
  ref -> {{ textEl }}
</template>

<script>
export default {
  data() {
    return {
      textEl: null,
    };
  },

  methods: {
    textRef(el) {
      this.textEl = el;
    },
  },
  computed: {
    getEl() {
      return this.textEl;
    },
  },
  mounted() {
    console.log('textEl', this.textEl);
  },
};
</script>
