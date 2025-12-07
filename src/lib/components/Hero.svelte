<script lang="ts">
  export let image: string;
</script>

<section class="relative h-[80vh] w-full overflow-hidden bg-gray-900">
  <img
    src={image}
    alt="Hero"
    class="h-full w-full object-cover"
  />
  <div class="absolute bottom-8 right-8 text-xs font-medium text-white/70 uppercase tracking-widest">
    Sound: Off
  </div>
</section>
