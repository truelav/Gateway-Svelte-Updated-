<script>
  import { recycleInfo } from "../data/recycle.json"
  import RecycleState from "../components/RecycleState.svelte";
  import PageTransition from '../components/PageTransition.svelte'
  export const states = recycleInfo

</script>

<PageTransition>
  <section class="text-gray-600 body-font overflow-hidden">
    <div class="container px-5 py-24 mx-auto">
      <div class="-my-8 divide-y-2 divide-gray-100">
        {#each states as item}
        
        <RecycleState {item}/>
  
        {/each}
  
      </div>
    </div>
  </section>
</PageTransition>

<style>

</style>