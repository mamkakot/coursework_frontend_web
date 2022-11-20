<template>
  <v-card class="mx-auto d-flex flex-row"
          width="600"
          variant="outlined">
    <v-img
        class="align-end text-white"
        height="200"
        max-width="300"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
        cover>
    </v-img>
    <div class="d-flex flex-column pt-4">
      <v-card-title> {{room.name}} </v-card-title>
      <v-card-subtitle class="pt-4">
         #{{ room.id }}
      </v-card-subtitle>
      <v-card-text class="d-flex flex-column align-content-start">
        <div>Статус комнаты:</div>
        <v-progress-linear :model-value="room.sum_status"></v-progress-linear>
      </v-card-text>
      <v-card-actions>
        <v-btn variant="outlined">
          Создать задачу
        </v-btn>

        <v-btn variant="outlined">
          Переименовать
        </v-btn>
      </v-card-actions>
    </div>
  </v-card>
</template>

<script>
// import {ref} from 'vue'

export default {
  name: "RoomCard",
  props: {
    room: {
      id: Number,
      name: String,
      sum_status: Number
    }
  },
  // setup(props){
  //   const sas = ref(props.id + props.name)
  //   return sas
  // }
}
</script>

<style scoped>

</style>