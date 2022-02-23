<script>
  export let item
</script>

<div class="md:w-1/3 sm:w-1/2">
  <div class="p-4 product-tablet-wrapper border-2 border-gray-200 m-3 rounded-2xl hover:bg-slate-100">
    <div class="rounded-lg h-64 overflow-hidden">
      <img alt="content" class="object-contain object-center h-full w-full" src={item.image}>
    </div>
    <h2 class="text-xl font-large title-font mt-5">{item.header}</h2>
    <p class="text-base leading-relaxed mt-2 mb-2 italic">Model: {item.id}</p>
  
    <div data-bv-show="rating_summary" data-bv-product-id={item.id}></div>

    <ul class="product-tablet-list list-disc ml-4 mt-2">
      {#each {length: 3}  as _ , bulletPoint}
        <li class="list-disc">{item.bulletPoints[bulletPoint]}</li>
      {/each}
    </ul>
  
    <div class="flex justify-space">
      <button class="text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-md m-1 mt-4">Buy Now</button>
      
      <a href={`/Product/${item.id}`}>
        <button class="text-white bg-slate-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-md m-1 mt-4">
          Learn More
        </button>
      </a>
    </div>

  </div>
</div>

<style>
  .product-tablet-list{
    max-width: 275px;
  }
</style>