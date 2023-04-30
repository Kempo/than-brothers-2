<script setup>
defineProps({
  itemNum: {
    type: Number,
    required: true,
  },
  itemTitle: {
    type: String,
    required: true,
  },
  itemDesc: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="individual-item">
    <h2>{{ itemNum }}. {{ itemTitle }}</h2>
    <p>{{ itemDesc }}</p>
  </div>
</template>
<!-- 
<script>
export default {
  props: ['itemNum', 'itemTitle', 'itemDesc']
}
</script> -->

<style lang="scss" scoped>
h2 {
  margin: 5px 0px;
}

.individual-item {
  h2 {
    font-weight: 700;
  }
  p {
    font-family: "Lato", sans-serif;
  }
}
@media screen and (max-width: 749px) {
  .individual-item {
    h2 {
      font-size: 1.25em;
    }
    p {
      font-size: 1em;
    }
  }
}
@media screen and (min-width: 750px) {
  .individual-item {
    h2 {
      font-size: 1.25em;
    }
    p {
      font-size: 1em;
    }
  }
}
</style>
