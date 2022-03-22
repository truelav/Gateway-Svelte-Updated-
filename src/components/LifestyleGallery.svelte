<script>
  import lifestyleImage1 from '/images/Lifestyle/lifestyle1.jpg'
  import lifestyleImage2 from '/images/Lifestyle/lifestyle2.jpg'
  import lifestyleImage3 from '/images/Lifestyle/lifestyle3.jpg'
  import lifestyleImage4 from '/images/Lifestyle/lifestyle4.jpg'
  import lifestyleImage5 from '/images/Lifestyle/lifestyle5.jpg'
</script>

<section class="overflow-hidden text-gray-700">
  <div class="container px-5 pb-12  py-2 mx-auto lg:pt-6 lg:pb-12">
    <div class="flex flex-wrap -m-1 md:-m-2">
      <div class="flex flex-wrap w-1/2">
        <div class="w-1/2 p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage2}
            data-aos="zoom-in"
            data-aos-delay="0"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
        <div class="w-1/2 p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage3}
            data-aos="zoom-in"
            data-aos-delay="300"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
        <div class="w-full p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage1}
            data-aos="zoom-in"
            data-aos-delay="600"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
      </div>
      <div class="flex flex-wrap w-1/2">
        <div class="w-full p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage5}
            data-aos="zoom-in"
            data-aos-delay="900"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
        <div class="w-1/2 p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage4}
            data-aos="zoom-in"
            data-aos-delay="900"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
        <div class="w-1/2 p-1 md:p-2 img-wrapper rounded-lg">
          <img alt="gallery" class="block object-cover object-center w-full h-full rounded-lg"
            src={lifestyleImage3}
            data-aos="zoom-in"
            data-aos-delay="600"
            data-aos-duration="300"
            data-aos-easing="ease-in-out">
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .img-wrapper {
      display: inline-block; /* change the default display type to inline-block */
      overflow: hidden;      /* hide the overflow */
  }

  .img-wrapper > img:hover {
    transform:scale(1.3);
    -ms-transform:scale(1.3); /* IE 9 */
    -moz-transform:scale(1.3); /* Firefox */
    -webkit-transform:scale(1.3); /* Safari and Chrome */
    transition: 0.8s ease-in-out;
    transition-delay: 100;
  }
</style>
