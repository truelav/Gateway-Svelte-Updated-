<script>
  import { onMount } from 'svelte';

  import {dataProducts} from '../data/allProducts.json'

  import PageTransition from '../components/PageTransition.svelte'
  import ProductTopHero from '../components/ProductTopHero.svelte'
  import ProductDimensions from '../components/ProductDimensions.svelte'
  import ProductLifestyle from '../components/ProductLifestyle.svelte'
  import LifestyleGallery from '../components/LifestyleGallery.svelte'
  import ProductSpecs from '../components/ProductSpecs.svelte'
  import ProductPorts from '../components/ProductPorts.svelte'

  export let params;

  const productData = dataProducts.filter((item) => item.id == params.id)[0]
</script>


<PageTransition>
  <!-- Top Hero Section -->
  <ProductTopHero {productData}/>
  
  <!-- Dimensions Sections -->
  <ProductDimensions {productData}/>
  
  <div class="backgroundSpots">
  
    <ProductLifestyle {productData}/>
    
    <ProductSpecs {productData}/>
    
    <ProductPorts {productData} />
    
    <LifestyleGallery />
  
    <!-- <ProductRatings /> -->
  
  </div>
</PageTransition>


<style>

</style>