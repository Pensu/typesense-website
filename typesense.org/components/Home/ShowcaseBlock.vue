<template>
  <a :href="link" target="_blank" class="text-dark">
    <div
      class="showcase-block border border-light px-5 py-4 d-flex align-items-center"
    >
      <h5 class="mb-0">
        {{ emoji }}<br />

        <slot name="title"></slot>
      </h5>
    </div>
  </a>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Showcase Title',
    },
    link: {
      type: String,
      default: '/#',
    },
    emoji: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
.showcase-block {
  max-width: 300px;
  min-width: 300px;
  min-height: 150px;

  @media (min-width: map-get($grid-breakpoints, 'sm')) {
    min-width: 200px;
  }

  h5 {
    line-height: 1.3;
  }

  a {
    border-bottom: unset;
  }
}
</style>
