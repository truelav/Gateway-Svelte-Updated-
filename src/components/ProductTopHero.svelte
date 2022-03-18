<script>
  export let productData
  import ProductRatingSummary from './ProductRatingSummary.svelte';
  import walmartIcon from '/images/Icons/walmart.png'
  import windowsIcon from '/images/Icons/windows11.png'
</script>


<section class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto flex flex-wrap">
    <div class="lg:w-1/2 w-full mb-10 lg:mb-0 rounded-lg overflow-hidden">
      <img alt={productData.productPage.imageTopSource.alt} class="object-contain object-center h-full w-full" src={productData.productPage.imageTopSource.src}
      data-aos="zoom-in"
      data-aos-duration="800"
      data-aos-easing="ease-in-out"
      data-aos-once="false">
    </div>

    <div class="flex flex-col flex-wrap lg:py-6 -mb-10 lg:w-1/2 lg:pl-12 lg:text-left text-center">
      <div class="flex flex-col mb-10 lg:items-start items-center">
        <div class="flex-grow">
          <div             
          data-aos="fade-left"
          data-aos-delay="500"
          data-aos-duration="500"
          data-aos-easing="ease-in-out"
          data-aos-once="false">
            <h2 class="text-gray-900 text-4xl title-font font-medium mb-3">{productData.header}</h2>
            <p class="leading-relaxed text-base italic">Model: {productData.id}
            </p>

            <ProductRatingSummary />

            <p class="leading-relaxed text-base my-5">{productData.description}
            </p>
            <div class="flex mt-6 items-center pb-5 border-b-2 border-gray-100 mb-5">
              <div class="flex">
                <span class="mr-3">Available Colors:</span>
                {#each productData.colors as color}
                <div class="px-2">
                  <button class="border-2 border-gray-300 ml-1 rounded-full w-8 h-8 focus:outline-none btn-background-color-{color}"></button>
                  <p class="leading-relaxed text-s mt-2 mb-2 capitalize text-center">{color}</p>
                </div>
                {/each}
              </div>
            </div>
          </div>
          
          {#if productData.windowsActivation}
            <div class=" divide-y-2 divide-gray-100">
              <div class=" flex-wrap md:flex-nowrap">
                <div class="md:w-64 md:mb-0 mb-6 flex-shrink-0 flex flex-col">
                  <img class="m-auto" src={windowsIcon} alt="Free Upgrade when available windows 11">
                </div>
                <div class="md:flex-grow">
                  <p class="leading-relaxed text-xs mt-2 mb-2">{productData.windowsActivation.p1}</p>
                  <p class="leading-relaxed text-xs mb-2">{productData.windowsActivation.p2}</p>
                  <p class="leading-relaxed text-xs italic text-indigo-600">
                    (see <a href={productData.windowsActivation.p1}>aka.md/windows11-spec</a> )
                  </p>
                </div>
              </div>
            </div>
          {/if}

          <ul class="my-5"
          data-aos="fade-left"
          data-aos-delay="1000"
          data-aos-duration="500"
          data-aos-easing="ease-in-out"
          data-aos-once="false">
            {#each productData.bulletPoints as bullet}
              <li class="list-disc mx-5 italic md:text-left">{bullet}</li>
            {/each}
          </ul>
          <div class="flex column justify-between">
            <button class="text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg">Buy Now</button>
            <div class="ml-6 lg:center items-center">
              <p class="leading-relaxed text-sm w-1/2 exclusive-at-walmart">Available exclusively at:</p>
              <img class="w-1/3" src={walmartIcon} alt="Exclusive At Walmart">
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>



<style>
  .exclusive-at-walmart {
    color: #0971ce;
  }

  .btn-background-color-black {
    background-color: #111111;
  }

  .btn-background-color-gray {
    background-color: #696f6d;
  }

  .btn-background-color-blue {
    background-color: #58a2df;
  }

  .btn-background-color-green {
    background-color: #5b736e;
  }

  .btn-background-color-red {
    background-color: #b9353b;
  }

  .btn-background-color-purple {
    background-color: #5135e2;
  }


</style>