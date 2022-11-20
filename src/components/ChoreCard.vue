<template>
  <v-card class="mx-auto d-flex flex-row"
          width="800"
          variant="outlined">
    <v-img
        class="align-end text-white"
        height="200"
        max-width="300"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
        cover>
      <v-card-title>This is a title of a chore</v-card-title>
    </v-img>
    <div class="d-flex flex-column">
      <v-card-subtitle class="pt-4">
        This is a subtitle of chore #{{ id }}
      </v-card-subtitle>
      <v-card-text>
        <div>Whitehaven Beach</div>

        <div>This is content of a chore</div>
      </v-card-text>
      <v-card-actions>
        <v-btn variant="outlined">
          Share
        </v-btn>

        <v-btn variant="outlined">
          Explore
        </v-btn>
      </v-card-actions>
    </div>
  </v-card>
</template>

<script>
export default {
  name: "ChoreCard",
  props: {
    id: Number,
    theme: String,
  }
}
</script>

<style scoped>

</style>