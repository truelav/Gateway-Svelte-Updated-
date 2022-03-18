<script>
  import PageTransition from '../components/PageTransition.svelte'
  import DropDownButton from '../components/DropDownButton.svelte';
  import SupportTablet from '../components/SupportTablet.svelte';
  import {supportProducts} from '../data/support.json'
</script>

<PageTransition>
  <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 py-24 mx-auto">
      <div class="grid sm:grid-cols-1 lg:grid-cols-2 gap-4 divide-y-2 divide-gray-100 ">
        {#each supportProducts as item}
    
        <SupportTablet {item} />
  
        {/each}
  
      </div>
    </div>
  </section>
</PageTransition>

<style>
  
</style>