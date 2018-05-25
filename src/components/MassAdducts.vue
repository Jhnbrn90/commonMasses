<template>
<div>

<h2>Common Mass Adducts</h2>

 Mass: <input type="text" v-model="mass"> g/mol
  <ul class="adducts">
    <li :key="adduct" v-for="adduct in Object.keys(adducts)">
      {{ adductMass(adduct) }} 
      <span class="small">({{ adduct }})</span>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      adducts: {
        'H': 1,
        'Na': 23,
        'MeOH + H': 33,
        'CH3CN + H': 42,
        'Et2NH + H': 74,
        'DEA + MeOH + H': 107
      },
      mass: '',
    };
  },

  methods: {
    adductMass(adduct) {
      return this.adducts[adduct]*1 + this.mass*1;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

input {
  text-align: center;
  width: 35px;
  border: 1px solid grey;
  margin: 5px;
  padding: 2px 5px;
  display: inline-block;
  border-radius: 8px;
}

.small {
  font-weight: 200;
  font-size: 12px;
}

h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 5px;
}
</style>
