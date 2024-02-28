<template>
  <div class="home" style="margin-left: 60px;">
    <h1>Homepage</h1>
    <v-btn prepend-icon="mdi-check-circle">
      <template v-slot:prepend>
          <v-icon color="success"></v-icon>
      </template>
      Button
    </v-btn>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({

});
</script>
