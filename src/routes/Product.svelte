<script>
  import { onMount } from 'svelte';

  import {dataProducts} from '../data/allProducts.json'

  import ProductTopHero from '../components/ProductTopHero.svelte'
  import ProductDimensions from '../components/ProductDimensions.svelte'
  import ProductLifestyle from '../components/ProductLifestyle.svelte'; 
  import LifestyleGallery from '../components/LifestyleGallery.svelte'
  import ProductSpecs from '../components/ProductSpecs.svelte'
  import ProductPorts from '../components/ProductPorts.svelte';

  export let params;

  const productData = dataProducts.filter((item) => item.id == params.id)[0]
</script>


<!-- Top Hero Section -->
<ProductTopHero {productData}/>

<!-- Dimensions Sections -->
<ProductDimensions />

<div class="backgroundSpots">

  <!-- Features Section -->
  <ProductSpecs {productData}/>

  <ProductLifestyle {productData}/>
  
  <ProductPorts {productData} />
  
  <LifestyleGallery />
  
</div>

<style>

</style>