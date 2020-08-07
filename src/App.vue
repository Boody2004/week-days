<template>
  <v-app>
    <v-main>
      <WeekDays/>
    </v-main>
  </v-app>
</template>

<script>
import WeekDays from './components/WeekDays';

export default {
  name: 'App',

  components: {
    WeekDays,
  },

  data: () => ({
    //
  }),
};
</script>
