<template>
  <div>
    <lv-card-list :width="300" />
    <lv-card-list primaryColor="#607c8a" secondaryColor="#8aa6b5" />
    <!-- REFACTORING -->
  </div>
</template>

<script>
import LvCardList from 'lightvue/skeleton/preset/CardList.vue';
export default {
  components: {
    LvCardList,
  },
};
</script>
