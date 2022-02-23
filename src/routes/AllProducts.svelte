<script>
  
  import {dataProducts} from '../data/allProducts.json'
  import ProductTablet from '../components/ProductTablet.svelte';
  export const allProducts = dataProducts

</script>

<section class="text-gray-600 body-font">
  <div class="backgroundSpots">
    <div class="container px-5 py-24 mx-auto">
      <div class="">
        
      </div>
      <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4">
  
        {#each dataProducts as item}
  
          <ProductTablet {item}/>
  
        {/each}
  
      </div>
    </div>
  </div>
</section>

<style>

</style>