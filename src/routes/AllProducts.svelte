<script>
  
  import {dataProducts} from '../data/allProducts.json'
  import ProductTablet from '../components/ProductTablet.svelte';
  export const allProducts = dataProducts

  let filteredProducts = [...dataProducts]
  const checkedHash = {
    "all": true,
    "gaming": false,
    "twoinone": false,
    "ultraslim": false,
    "convertible": false
  }
  console.log(filteredProducts)

  const handleFilter = (event) => {
    checkedHash[event] = !checkedHash[event]
    console.log(checkedHash[event])

    // filteredProducts = filteredProducts.filter((item) => {
    //   return checkedHash[item.category]
    // })

  }

</script>

<section class="text-gray-600 body-font">
  <div class="backgroundSpots">

    <div class="container px-5 py-24 mx-auto">

      <div class="mb-6">
        <div class="block">
          <span class="text-gray-700">Checkboxes</span>
          <div class="mt-2">
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="all" bind:checked="{checkedHash.all}" on:input="{() => handleFilter("all")}" >
                <span class="ml-2">All Series</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="twoinone" bind:checked="{checkedHash.twoinone}" on:input="{() => handleFilter("twoinone")}" >
                <span class="ml-2">2 In One</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim" bind:checked="{checkedHash.convertible}"  on:input="{() => handleFilter("convertible")}">
                <span class="ml-2">Convertible</span>
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