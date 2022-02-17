<script>
  import dimensionsTopImage from '/images/Lifestyle/dimensions-top-image.jpg'
  import dimensionsBotImage from '/images/Lifestyle/dimensions-bot-image.jpg'
  import dimensionsOutlineImage from '/images/Lifestyle/outline.jpg'
</script>



<section class="product-specs-sections">
  <div class="product-specs-border-image-container">
    <img src={dimensionsTopImage} class="footer-top-image" alt="footer gateway wave image">
  </div>
  <div class="product-specs-container">

      <div class="product-specs-top-container">
          <div class="product-specs-top-inner-container grid grid-cols-3">

            <div class="flex  flex-col content-center m-auto">
              <h2 class="text-gray-900 text-lg title-font font-medium mb-3">Inside Box</h2>
              <p>
                  Gateway Laptop
              </p>
              <p>
                  Laptop Charger
              </p>
              <p>
                  Warranty Book
              </p>
              <p>
                  Quick Start Guide
              </p>
            </div>

            <img src={dimensionsOutlineImage} class="product-outline-image" alt="gateway outline laptop">

            <div class="flex  flex-col content-center m-auto">
              <h2 class="text-gray-900 text-lg title-font font-medium mb-3">Product Dimensions</h2>
              <p>
                  Product Dimensions
              </p>
              <p>
                  Length: 15.58”
              </p>
              <p>
                  Height: 10.27”
              </p>
              <p>
                  Width: 1.10"
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
</style>