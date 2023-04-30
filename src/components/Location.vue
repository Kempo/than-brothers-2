<script setup>
defineProps({
  LocName: {
    type: String,
    required: true,
  },
  TimeSchedule: {
    type: String,
    required: true,
  },
  Address: {
    type: String,
    required: true,
  },
  Phone: {
    type: String,
    required: true,
  },
  City: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="individual-item">
    <h2>
      <a :href="getLink" target="_blank" rel="noopener noreferrer">
        {{ LocName }} <span v-if="TimeSchedule === 2">*</span>
      </a>
    </h2>
    <p>{{ Address }} {{ City }}</p>
    <p>{{ Phone }}</p>
  </div>
</template>
<script>
export default {
  computed: {
    getLink: function () {
      return (
        "https://www.google.com/maps/search/?api=1&query=" +
        encodeURIComponent(`${this.Address} ${this.City}`)
      );
    },
  },
};
</script>

<style lang="scss" scoped>
p {
  font-style: italic;
  color: rgb(101, 100, 100);
  margin: 5px;
}
h2 {
  margin: 10px;
}
a {
  text-decoration: none;
  color: $blue;
}
a:hover {
  cursor: pointer;
  color: $red;
}
.individual-item {
  width: auto !important;
  font-size: 1em;
  padding-right: 20px;
  margin: 20px 0px;
}
</style>
