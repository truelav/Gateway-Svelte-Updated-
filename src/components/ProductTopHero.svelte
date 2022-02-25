<script>
  export let productData
  import ProductRatingSummary from './ProductRatingSummary.svelte';
  import walmartIcon from '/images/Icons/walmart.png'
</script>


<section class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto flex flex-wrap">
    <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
      <img alt={productData.productPage.imageTopSource.alt} class="object-contain object-center h-full w-full" src={productData.productPage.imageTopSource.src}>
    </div>

    <div class="flex flex-col flex-wrap lg:py-6 -mb-10 lg:w-1/2 lg:pl-12 lg:text-left text-center">
      <div class="flex flex-col mb-10 lg:items-start items-center">
        <div class="flex-grow">
          <h2 class="text-gray-900 text-4xl title-font font-medium mb-3">{productData.header}</h2>
          <p class="leading-relaxed text-base italic">Model: {productData.id}</p>
          <ProductRatingSummary />  
          <p class="leading-relaxed text-base my-5">{productData.description}</p>
          <ul class="my-5">
            {#each productData.bulletPoints as bullet}
              <li class="list-disc mx-5 italic">{bullet}</li>
            {/each}
          </ul>
          <button class="flex text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg">Buy Now</button>
        </div>

        {#if productData.windowsActivation}
          <p class="leading-relaxed text-sm mt-2 mb-2">{productData.windowsActivation.p1}</p>
          <p class="leading-relaxed text-sm mb-2">{productData.windowsActivation.p2}</p>
          <p class="leading-relaxed text-sm italic text-indigo-600">
            (see <a href={productData.windowsActivation.p1}>aka.md/windows11-spec</a> )
          </p>
        {/if}

      </div>

      <div class="flex mt-6 items-center pb-5 border-b-2 border-gray-100 mb-5">
        <div class="flex">
          <span class="mr-3">Available Colors:</span>
          <button class="border-2 border-gray-300 rounded-full w-6 h-6 focus:outline-none"></button>
          <button class="border-2 border-gray-300 ml-1 bg-gray-700 rounded-full w-6 h-6 focus:outline-none"></button>
          <button class="border-2 border-gray-300 ml-1 bg-indigo-500 rounded-full w-6 h-6 focus:outline-none"></button>
        </div>
      </div>

      <div class="flex mb-10 lg:center items-center">
        <p class="leading-relaxed text-xl w-1/2 exclusive-at-walmart">Available exclusively at:</p>
        <img class="w-1/3" src={walmartIcon} alt="Exclusive At Walmart">
      </div>
    </div>
  </div>
</section>

<style>
  .exclusive-at-walmart {
    color: #0971ce;
  }
</style>