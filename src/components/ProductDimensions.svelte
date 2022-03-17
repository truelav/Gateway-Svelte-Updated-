<script>
  import dimensionsTopImage from '/images/Lifestyle/dimensions-top-image.jpg'
  import dimensionsBotImage from '/images/Lifestyle/dimensions-bot-image.jpg'
  import dimensionsOutlineImage from '/images/Lifestyle/outline.jpg'

  export let productData
</script>



<section class="product-specs-sections">
  <div class="product-specs-border-image-container">
    <img src={dimensionsTopImage} class="footer-top-image" alt="footer gateway wave" >
  </div>
  <div class="product-specs-container">

      <div class="product-specs-top-container">
          <div class="product-specs-top-inner-container grid grid-cols-3">

            <div class="flex  flex-col content-center m-auto">
              <h2 class="sm:text-3xl text-xl font-medium title-font mb-4 text-gray-900 s-FcQS7QhyxSEx">Inside Box</h2>
              <div class="">
                <p class="m-2">
                    Gateway Laptop
                </p>
                <p class="m-2">
                    Laptop Charger
                </p>
                <p class="m-2">
                    Warranty Book
                </p>
                <p class="m-2">
                    Quick Start Guide
                </p>
              </div>
            </div>

            <img src={dimensionsOutlineImage} class="product-outline-image" alt="gateway outline laptop">

            <div class="flex  flex-col content-center m-auto">
              <h2 class="sm:text-3xl text-xl font-medium title-font mb-4 text-gray-900 s-FcQS7QhyxSEx">Product Dimensions</h2>
              <p class="m-2">
                  Length: {productData.dimensions.length}”
              </p>
              <p class="m-2">
                  Height: {productData.dimensions.height}”
              </p>
              <p class="m-2">
                  Width: {productData.dimensions.width}"
              </p>
            </div>
        </div>
    </div>
  </div>
  <div class="product-specs-border-image-container">
    <img src={dimensionsBotImage} class="footer-top-image" alt="footer gateway wave image">
  </div>
</section>


<style>
  .product-specs-sections {
    background-color: #e0e7ff;
  }

  .footer-top-image {
    width: 100vw;
  }
</style>