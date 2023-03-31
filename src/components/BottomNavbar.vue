<template>
 <v-bottom-navigation v-model="value">
    <v-btn value="recent" @click="$router.push('/push')">
      <span>Recent</span>

      <v-icon>mdi-history</v-icon>
    </v-btn>

    <v-btn value="favorites">
      <span>Authors</span>

      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn value="nearby">
      <span>Memberd</span>

      <v-icon>mdi-badge-account</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>