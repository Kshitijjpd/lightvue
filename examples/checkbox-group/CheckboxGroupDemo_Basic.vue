<template>
  <div>
    <h4>Options as array of objects</h4>
    <lv-checkbox-group v-model="chosenCities1" name="cities" :options="cities" optionLabel="name" pulse color="primary"></lv-checkbox-group>
    <h6>Chosen options (using v-model): {{ chosenCities1 }}</h6>
    <br />
    <h4>Options as array of objects (With: optionValue="code")</h4>
    <lv-checkbox-group v-model="chosenCities2" name="cities" :options="cities" optionLabel="name" pulse color="primary" optionValue="code"></lv-checkbox-group>
    <h6>Chosen options (using v-model): {{ chosenCities2 }}</h6>
    <br />
    <h4>Options as array of strings</h4>
    <lv-checkbox-group v-model="chosenCities3" name="countries" :options="countries" color="primary"></lv-checkbox-group>
    <h6>Chosen options (using v-model): {{ chosenCities3 }}</h6>
    <br />
    <h4>Options as array of strings [No Preselected]</h4>
    <lv-checkbox-group v-model="chosenCities4" name="countries" :options="countries" color="primary"></lv-checkbox-group>
    <h6>Chosen options (using v-model): {{ chosenCities4 }}</h6>
  </div>
  <!-- REFACTORING -->
</template>

<script>
import LvCheckboxGroup from 'lightvue/checkbox-group';
export default {
  components: {
    LvCheckboxGroup,
  },
  data() {
    return {
      cities: [
        { name: 'New York', code: 'NY' },
        { name: 'Rome', code: 'RM', disabled: true },
        { name: 'London', code: 'LDN' },
        { name: 'Istanbul', code: 'IST', checked: true },
        { name: 'Paris', code: 'PRS' },
      ],
      countries: ['India', 'USA', 'Japan', 'France'],
      chosenCities1: [{ name: 'Paris', code: 'PRS' }],
      chosenCities2: ['LDN', 'NY'],
      chosenCities3: ['USA'],
      chosenCities4: null,
    };
  },
};
</script>
