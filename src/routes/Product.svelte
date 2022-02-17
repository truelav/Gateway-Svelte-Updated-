<script>
  import { onMount } from 'svelte';

  import {dataProducts} from '../data/allProducts.json'

  import ProductTopHero from '../components/ProductTopHero.svelte'
  import ProductDimensions from '../components/ProductDimensions.svelte'
  import ProductFeatures from '../components/ProductFeatures.svelte';
  import ProductPorts from '../components/ProductPorts.svelte';

  export let params;

  const productData = dataProducts.filter((item) => item.id == params.id)[0]
</script>


<!-- Top Hero Section -->
<ProductTopHero {productData}/>

<div class="backgroundSpots">

  <!-- Dimensions Sections -->
  <ProductDimensions />
  
  <!-- Features Section -->
  <ProductFeatures />
  
  <ProductPorts {productData} />

</div>

<style>

</style>