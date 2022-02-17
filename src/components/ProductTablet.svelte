<script>
  export let item
</script>

<div class="p-4 md:w-1/3 sm:mb-0 mb-6 ">
  <div class="rounded-lg h-64 overflow-hidden">
    <img alt="content" class="object-contain object-center h-full w-full" src={item.image}>
  </div>
  <h2 class="text-xl font-large title-font text-gray-900 mt-5">{item.header}</h2>
  <p class="text-base leading-relaxed mt-2">Model: {item.id}</p>

  <ul class="list-none">
    {#each item.bulletPoints as bulletPoint}
      <li>{bulletPoint}</li>
    {/each}
  </ul>

  <a class="text-blue-500 inline-flex items-center mt-3" href={`/Product/${item.id}`}>Learn More
    <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-2" viewBox="0 0 24 24">
      <path d="M5 12h14M12 5l7 7-7 7"></path>
    </svg>
  </a>
</div>