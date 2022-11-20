<template>
  <div class="d-flex align-center flex-column">
    <ChoreCard class="mt-4" v-for="i in 10" :id="i" :theme="theme" :key="i"></ChoreCard>
  </div>
</template>

<script>
import ChoreCard from "@/components/ChoreCard";

export default {
  name: "ChoresList",
  components: {
    ChoreCard
  },
  props: {
    theme: String,
  }
}
</script>

<style scoped>

</style>