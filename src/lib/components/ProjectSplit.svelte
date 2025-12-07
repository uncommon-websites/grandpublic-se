<script lang="ts">
  export let left: { client: string; services: string; image: string; textColor?: string };
  export let right: { client: string; services: string; image: string; textColor?: string };
</script>

<section class="flex flex-col md:flex-row w-full h-[85vh] md:h-[70vh]">
  <!-- Left Item -->
  <div class="relative w-full md:w-1/2 h-full group overflow-hidden">
    <img
      src={left.image}
      alt={left.client}
      class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
    />
    <div class="absolute inset-0 bg-black/10 transition-opacity group-hover:bg-black/20"></div>
    
    <div class="absolute left-0 top-0 p-6 md:p-10 flex flex-col items-start gap-1 z-10">
      <span class="{left.textColor || 'text-white'} text-sm font-bold tracking-wide">{left.client}</span>
      <span class="{left.textColor || 'text-white'} text-xs opacity-90 tracking-wide max-w-[250px] leading-relaxed">
        {left.services}
      </span>
    </div>
  </div>

  <!-- Right Item -->
  <div class="relative w-full md:w-1/2 h-full group overflow-hidden">
    <img
      src={right.image}
      alt={right.client}
      class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
    />
    <div class="absolute inset-0 bg-black/10 transition-opacity group-hover:bg-black/20"></div>

    <div class="absolute left-0 top-0 p-6 md:p-10 flex flex-col items-start gap-1 z-10">
      <span class="{right.textColor || 'text-white'} text-sm font-bold tracking-wide">{right.client}</span>
      <span class="{right.textColor || 'text-white'} text-xs opacity-90 tracking-wide max-w-[250px] leading-relaxed">
        {right.services}
      </span>
    </div>
  </div>
</section>
