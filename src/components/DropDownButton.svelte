<script>
  export let item
  let drivers = item.drivers
  console.log(drivers)
</script>


<div class="p-8 pl-0">
  <p class="leading-relaxed">All the Drivers can be download individualy.</p>
  <div class="dropdown inline-block relative">
    <button class="bg-gray-300 text-gray-700 font-semibold py-2 px-4 rounded inline-flex items-center">
      <span class="mr-1">Download Drivers</span>
      <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/> </svg>
    </button>
    <ul class="dropdown-menu absolute hidden text-gray-700 pt-1 z-50">
      {#each drivers as driver}
        <li class="w-80"><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="{driver.link}" download="{driver.link}">{driver.name}</a></li>
      {/each}
    </ul>
  </div>

</div>


<style>
  .dropdown:hover .dropdown-menu {
    display: block;
  }
</style>