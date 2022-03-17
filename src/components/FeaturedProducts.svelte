<script>
    import {dataProducts} from '../data/allProducts.json'
    export let allProducts = dataProducts.filter((item) => item.featured === "yes")
    import ProductTablet from './ProductTablet.svelte';
</script>


<section class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto">
    <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4">
      {#each allProducts as item}
        <ProductTablet {item}/>
      {/each}
    </div>
  </div>
</section>


<style>

</style>