<script setup lang="ts">
import Location from "@/components/Location.vue";
</script>

<template>
  <div id="location">
    <div class="layout">
      <section>
        <h1>Locations</h1>
        <ul class="times">
          <li v-for="t in times" v-bind:key="t.id">{{ t.time }}</li>
        </ul>
        <Location
          v-for="loc in list"
          v-bind:key="loc.id"
          v-bind:loc-name="loc.title"
          v-bind:Address="loc.address"
          v-bind:Phone="loc.phone"
          v-bind:City="loc.city"
          v-bind:TimeSchedule="loc.timeSchedule"
        />
      </section>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data: function () {
    return {
      list: [
        {
          id: 1,
          timeSchedule: 1,
          title: "Aurora",
          address: "7800 Aurora Ave. N",
          city: "Seattle WA 98103",
          phone: "(206) 527-5973",
        },
        {
          id: 2,
          timeSchedule: 2,
          title: "Broadway",
          address: "527 Broadway E",
          city: "Seattle WA 98102",
          phone: "(206) 568-7218",
        },
        {
          id: 3,
          timeSchedule: 1,
          title: "University of Washington",
          address: "4207 University Way",
          city: "Seattle WA 98105",
          phone: "(206) 632-7272",
        },
        {
          id: 4,
          timeSchedule: 2,
          title: "Wallingford",
          address: "2309 N 45th St",
          city: "Seattle WA 98103",
          phone: "(206) 632-7378",
        },
        {
          id: 5,
          timeSchedule: 1,
          title: "Lynnwood",
          address: "16809 Highway 99",
          city: "Lynnwood WA 98037",
          phone: "(425) 999-6596",
        },
        {
          id: 6,
          timeSchedule: 2,
          title: "Fremont",
          address: "626 N 34th St",
          city: "Seattle WA 98103",
          phone: "(206) 915-1928",
        },
      ],
      times: [
        { id: 1, time: "DAILY 10 - 9" },
        { id: 2, time: "(*) = 11 - 9" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#location {
  display: flex;
  justify-content: center;
  padding-top: 80px;

  .layout {
    .times {
      font-weight: 500;
      margin: 0px;
      padding: 0px;
    }
  }
}

h1 {
  @include section-title-size;
}
</style>
