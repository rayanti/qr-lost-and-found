<template>
  <div>
    <v-card
      class="mx-auto"
      tile
    >
      <v-toolbar>
        <v-app-bar-nav-icon @click.stop="show = !show"></v-app-bar-nav-icon>
        <v-toolbar-title>{{title}}</v-toolbar-title>
      </v-toolbar>
    </v-card>
    <Drawer :show.sync="show"/>
  </div>
</template>

<script>
import Drawer from '@/components/Drawer'

export default {
  name: "Header",
  components: {
    Drawer
  },
  data: () => ({
    show: false
  }),
  props: {
    title: String,
  },
};
</script>
