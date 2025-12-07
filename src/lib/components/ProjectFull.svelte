<script lang="ts">
  export let client: string;
  export let services: string;
  export let title: string;
  export let image: string;
  export let textColor: string = "text-white";
  export let overlayColor: string = "bg-black/20"; // Optional overlay for better contrast
  export let linkText: string = "View case";
  export let largeTextOverlay: string = ""; 
  export let largeTextOverlayClass: string = "text-white/20"; // Default class
</script>

<section class="relative h-[85vh] w-full overflow-hidden group">
  <div class="absolute inset-0">
    <img
      src={image}
      alt={title}
      class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-105"
    />
    {#if overlayColor}
      <div class="absolute inset-0 {overlayColor}"></div>
    {/if}
  </div>

  <div class="absolute left-0 top-0 p-6 md:p-12 lg:p-16 flex flex-col items-start gap-4 max-w-3xl z-10 pointer-events-none">
    <div class="flex flex-col gap-1 pointer-events-auto">
      <span class="{textColor} text-sm font-semibold tracking-wide">{client}</span>
      <span class="{textColor} text-xs md:text-sm opacity-80 tracking-wide">{services}</span>
    </div>
    
    <h2 class="{textColor} text-3xl md:text-4xl lg:text-5xl font-normal leading-tight mt-2 pointer-events-auto">
      {title}
    </h2>

    <a href="#" class="{textColor} mt-4 text-sm font-medium border-b border-current pb-0.5 hover:opacity-70 transition-opacity pointer-events-auto inline-block">
      {linkText}
    </a>
  </div>
  
  {#if largeTextOverlay}
    <div class="absolute inset-0 flex items-center justify-center pointer-events-none overflow-hidden">
       <span class="text-[15vw] font-bold uppercase tracking-widest text-center leading-none whitespace-nowrap {largeTextOverlayClass}">
         {@html largeTextOverlay}
       </span>
    </div>
  {/if}
</section>
