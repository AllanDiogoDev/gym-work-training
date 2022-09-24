<template>
  <div>
    <NavBar/>
    <AthletesList/>
    <!-- <SectionTypesExercises/> -->
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import AthletesList from './components/AthletesList.vue';
import 'material-icons/iconfont/material-icons.css';

// import SectionTypesExercises from './components/SectionTypesExercises.vue';

export default {
  name: 'App',
  components: {
    // SectionTypesExercises,
    NavBar,
    AthletesList,
}
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lora&family=Roboto+Slab&display=swap');

*{
    font-family: 'Lora', serif;
}
</style>
