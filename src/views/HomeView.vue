<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListDrinks from '../components/ListDrinks.vue'

let baseUrlSvg = ref("www.thecocktaildb.com/api/json/v1/1/search.php?f=m")
let strDrink = reactive(ref())

onMounted(() => {
  fetch("https://www.thecocktaildb.com/api/json/v1/1/search.php?f=m")
    .then(response => response.json())
    .then(response => {
      strDrink.value = response.results
      console.log(strDrink);
    });
})
</script>

<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-6">
          <div class="card" style="width: 18rem;">
            <img src="https:\/\/www.thecocktaildb.com\/images\/media\/drink\/metwgh1606770327.jpg" class="card-img-top" alt="...">
            <div class="card-body">
              <h2 class="card-title">Mojito</h2>
              <p class="card-text"></p>
            </div>
          </div>
        </div>

        <div class="col-sm-12 col-md-6">
          <div class="card" >
            <div class="card-body-row">
              <ListDrinks 
                v-for="strDrink in strDrinks"
                :key="strDrink.name"
                :name="strDrink.name"
                :baseUrlSvg="baseUrlSvg + strDrink.url.split('/')[6] + '.svg'"
                />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
