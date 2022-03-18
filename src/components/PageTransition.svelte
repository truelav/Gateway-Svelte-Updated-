<script>
  import { fly } from 'svelte/transition';
</script>

  <div
    in:fly="{{ y: -500, duration: 500, delay: 300 }}"
    out:fly="{{ y: -500, duration: 500 }}" 
  >
    <slot/>
  </div>

<style>
  
</style>  