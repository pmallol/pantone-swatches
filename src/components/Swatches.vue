<template>
  <div class="swatches">
    <div class="swatch"
      v-for="swatch in swatches"
      v-bind:swatch="swatch"
      v-bind:key="swatch.id"
      >
        <div class="color" :style="{ backgroundColor: swatch.color }"></div>
          <div class="description">
            <h2>PANTONE</h2>
            <p> {{ swatch.id }} </p>
        </div>
      </div>
  </div>
</template>

<script>
import { pantone } from '../assets/data/pantone-swatches'
export default {
  name: 'Swatches',
  data: function() {
return {
    swatches: pantone
  };
}
}
</script>

<style scoped>
.swatches {
  margin-top: 5rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  grid-gap: 2rem;
  justify-items: center;
}

.swatch {
  width: 220px;
  height: 335px;
  transition: ease-in .2s;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}

.swatch:hover {
  box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.2);
}

.swatch .color {
  flex-basis: 66%;
}

.swatch .description {
  flex-basis: 34%;
  background-color: #ffffff;
  font-weight: 900;
  padding: 15px;
}

.swatch h2 {
  font-weight: inherit;
  margin: .5rem 0;
}
</style>