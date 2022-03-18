<script>
  import PageTransition from '../components/PageTransition.svelte'
  import FeaturedProducts from '../components/FeaturedProducts.svelte'
  import headerImgLg from '/images/Windows11/header_xl.jpg'
  import pillar_blade_1 from '/images/Windows11/pillar_blade_1.jpg'
  import pillar_blade_2 from '/images/Windows11/pillar_blade_2.jpg'
  import pillar_blade_3 from '/images/Windows11/pillar_blade_3.jpg'
  import pillar_blade_4 from '/images/Windows11/pillar_blade_4.jpg'
  import pillar_blade_5 from '/images/Windows11/pillar_blade_5.jpg'
  import pillar_blade_6 from '/images/Windows11/blade_6.jpg'
  import m365_icons from '/images/Windows11/m365_icons.png'

</script>

<PageTransition>
  <section >
    <div class="container flex m-auto">
      <img class="" src="{headerImgLg}" alt="windows 11 Brings you closer to what you love">
    </div>
  </section>
  
  
  <div class="backgroundSpots">
  
    <FeaturedProducts />
    
    <section >
      <div class="container flex m-auto">
        <div class="grid grid-cols-2">
    
          <div class="">
            <img class="" src="{pillar_blade_1}" alt="windows 11 tablet gateway">
          </div>
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">Get a fresh perspective</h2>
            <p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
          </div>
    
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">Life's better together</h2>
            <p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
          </div>
          <div class="">
            <img class="" src="{pillar_blade_2}" alt="man with windows 11 tablet gateway video call">
          </div>
    
          <div class="">
            <img class="" src="{pillar_blade_3}" alt="windows 11 laptop gateway">
          </div>
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">What you need—when and where you need it.</h2>
            <p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
          </div>
    
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">Playtime. Anytime.</h2>
            <p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
          </div>
          <div class="">
            <img class="" src="{pillar_blade_4}" alt="windows 11 laptop gateway gaming">
          </div>
    
          <div class="">
            <img class="" src="{pillar_blade_5}" alt="windows 11 gateway series collection">
          </div>
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">Innovation for each of us.</h2>
            <p class="leading-relaxed">Glossier echo park pug, church-key sartorial biodiesel vexillologist pop-up snackwave ramps cornhole. Marfa 3 wolf moon party messenger bag selfies, poke vaporware kombucha lumbersexual pork belly polaroid hoodie portland craft beer.</p>
          </div>
    
          <div class="flex flex-col m-auto pl-8 pr-8">
            <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">The way to get things done</h2>
            <p class="leading-relaxed">With a Microsoft 365 subscription you get security, storage, and premium apps all for one low price.</p>
            <img class="max-w-xs mt-6" alt="Microsoft 365 | " src="{m365_icons}">
          </div>
          <div class="">
            <img class="" src="{pillar_blade_6}" alt="windows 11 laptop gateway gaming">
          </div>
    
        </div>
      </div>
    </section>
  
  </div>
</PageTransition>




<style>

</style>