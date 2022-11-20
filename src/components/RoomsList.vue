<template>
  <div class="d-flex align-center flex-column">
    <RoomCard class="mt-4" v-for="room in rooms" :room="room" :key="room.id"></RoomCard>
  </div>
</template>

<script>
import RoomCard from "@/components/RoomCard";
import {ref} from "vue";

export default {
  name: "RoomsList",
  components: {
    RoomCard
  },
  setup() {
    const rooms = ref([
      {
        "id": 1,
        "sum_status": 40,
        "name": "Kitchen"
      },
      {
        "id": 2,
        "sum_status": 50,
        "name": "Sleeping Room"
      },
      {
        "id": 3,
        "sum_status": 0,
        "name": "sas room"
      },
      {
        "id": 4,
        "sum_status": null,
        "name": "sas room"
      }
    ])

    return {rooms}
  }
}
</script>

<style scoped>

</style>