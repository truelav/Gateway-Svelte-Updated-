<script>
  import DropDownButton from '../components/DropDownButton.svelte';
  export let item
</script>

<div class="sm:py-0 py-8 pl-8 flex flex-wrap md:flex-nowrap">
  <div class="md:w-64 md:mb-0 mb-6 flex-shrink-0 flex flex-col">
    <img src="{item.image}" alt="{item.header}" class="md:w-full sm:w-4/6 support-product-image">
  </div>
  <div class="md:flex-grow border-gray-200 rounded-2xl">
    <h2 class="text-2xl font-medium text-gray-900 title-font mb-2">{item.id}</h2>
    <p class="leading-relaxed">{item.header}</p>
    <button class="bg-gray-300 text-gray-700 font-semibold py-2 px-4 rounded inline-flex items-center">
      <span class="mr-1">Download User Guide</span>
    </button>
    <DropDownButton {item}/>
  </div>
</div>

<style>
  .support-product-image {
    max-width: 250px;
  }
</style>