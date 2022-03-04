<script>
  
  import {dataProducts} from '../data/allProducts.json'
  import ProductTablet from '../components/ProductTablet.svelte';
  export const allProducts = dataProducts

  let filteredProducts = [...dataProducts]
  console.log(filteredProducts)

  const handleFilter = (event) => {
    console.log(event)
    if(event === ''){
      filteredProducts = dataProducts
    } else {
      filteredProducts = filteredProducts.filter((item) => item.category === event)
    }
  }

</script>

<section class="text-gray-600 body-font">
  <div class="backgroundSpots">

    <div class="container px-5 py-24 mx-auto">

      <div class="">
        <div class="block">
          <span class="text-gray-700">Checkboxes</span>
          <div class="mt-2">
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="2-in-one" on:input="{() => handleFilter("")}" >
                <span class="ml-2">All Series</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="2-in-one" on:input="{() => handleFilter("2-in-one")}" >
                <span class="ml-2">2 In One</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim" on:input="{() => handleFilter("ultra-slim")}">
                <span class="ml-2">Ultra Slim</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="gaming" on:input="{() => handleFilter("gaming")}">
                <span class="ml-2">Gaming</span>
              </label>
            </div>
          </div>
        </div>
      </div>


      <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4">
  
        {#each filteredProducts as item}
  
          <ProductTablet {item}/>
  
        {/each}
  
      </div>
    </div>
  </div>
</section>

<style>

</style>