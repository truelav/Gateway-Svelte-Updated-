<script>
  
  import {dataProducts} from '../data/allProducts.json'
  import ProductTablet from '../components/ProductTablet.svelte';
  export const allProducts = dataProducts

  let filteredProducts = [...dataProducts]

  const screenSizes  = {
    "17.3": false,
    "15.6": false,
    "13.3": false,
    "14.1": false,
    "11.6": false,
    "10.0": false
  }


  const checkedHash = {
    "gaming": false,
    "ultraslim": false,
    "convertible": false,
    "tablets": false
  }

  const handleFilterByScreen = (event) => {
    checkedHash[event] = !checkedHash[event]
    let showAllProducts = true;

    filteredProducts = dataProducts.filter((item) => {
      return checkedHash[item.category]
    })

    for(let key in checkedHash){
      showAllProducts = showAllProducts && !checkedHash[key]
    }

    console.log(showAllProducts)
    if(showAllProducts) filteredProducts = [...dataProducts]
  }

  const handleFilter = (event) => {
    checkedHash[event] = !checkedHash[event]
    let showAllProducts = true;

    filteredProducts = dataProducts.filter((item) => {
      return checkedHash[item.category]
    })

    for(let key in checkedHash){
      showAllProducts = showAllProducts && !checkedHash[key]
    }

    console.log(showAllProducts)
    if(showAllProducts) filteredProducts = [...dataProducts]
  }

</script>

<section class="text-gray-600 body-font">
  <div class="backgroundSpots">
    <div class="container px-5 py-24 mx-auto">
      <div class="mb-6">
        <div class="flex flex-wrap sm:-m-4 -mx-4 -mb-10 -mt-4">
          <div class="mt-2 lg:w-1/3 md:w-1/2 sm:w-1/2 p-4">
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim"  on:input="{() => handleFilter("convertible")}">
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
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="tablets" on:input="{() => handleFilter("tablets")}" >
                <span class="ml-2">Tablets</span>
              </label>
            </div>
          </div>

          <!-- Sizes categories -->
          <div class="mt-2 lg:w-1/3 md:w-1/2 sm:w-1/2 p-4">
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim" bind:checked="{checkedHash.convertible}"  on:input="{() => handleFilter("convertible")}">
                <span class="ml-2">17.3"</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim" on:input="{() => handleFilter("ultra-slim")}">
                <span class="ml-2">15.6"</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="gaming" on:input="{() => handleFilter("gaming")}">
                <span class="ml-2">14.1"</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="tablets" on:input="{() => handleFilter("tablets")}" >
                <span class="ml-2">13.3"</span>
              </label>
            </div>
          </div>

          <div class="mt-2 lg:w-1/3 md:w-1/2 sm:w-1/2 p-4">
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="ultra-slim" bind:checked="{checkedHash.convertible}"  on:input="{() => handleFilter("convertible")}">
                <span class="ml-2">11.6"</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="gaming" on:input="{() => handleFilter("gaming")}">
                <span class="ml-2">10.0"</span>
              </label>
            </div>
            <div>
              <label class="inline-flex items-center">
                <input type="checkbox" class="form-checkbox" value="tablets" on:input="{() => handleFilter("tablets")}" >
                <span class="ml-2">8.0"</span>
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