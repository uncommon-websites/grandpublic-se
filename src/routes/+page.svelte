<script lang="ts">
  import Hero from "$lib/components/Hero.svelte";
  import IntroText from "$lib/components/IntroText.svelte";
  import ProjectFull from "$lib/components/ProjectFull.svelte";
  import ProjectSplit from "$lib/components/ProjectSplit.svelte";
  import QuoteSection from "$lib/components/QuoteSection.svelte";
  import Footer from "$lib/components/Footer.svelte";

  // Image placeholders - trying to match the vibe
  const images = {
    hero: "https://images.unsplash.com/photo-1540555700478-4be289fbecef?q=80&w=2500&auto=format&fit=crop", // Water/Shower
    fagerhult: "https://images.unsplash.com/photo-1504333638930-c8787321eee0?q=80&w=2500&auto=format&fit=crop", // Dark blue mood
    craft: "https://images.unsplash.com/photo-1483721310020-03333e577078?q=80&w=1500&auto=format&fit=crop", // Runner
    crescent: "https://images.unsplash.com/photo-1485965120184-e220f721d03e?q=80&w=1500&auto=format&fit=crop", // Bike
    snif: "https://images.unsplash.com/photo-1615634260167-c8cdede054de?q=80&w=2500&auto=format&fit=crop", // Beige abstract
    nikon: "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?q=80&w=2500&auto=format&fit=crop", // Green mountains
    skoda: "https://images.unsplash.com/photo-1469854523086-cc02fe5d8800?q=80&w=2500&auto=format&fit=crop", // Desert road
    bebo: "https://images.unsplash.com/photo-1567538096630-e0c55bd6374c?q=80&w=1500&auto=format&fit=crop", // Chair
    head: "https://images.unsplash.com/photo-1534438327276-14e5300c3a48?q=80&w=1500&auto=format&fit=crop", // Dark gym/sports
    sture: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=2500&auto=format&fit=crop", // Fashion portrait
    xshore: "https://images.unsplash.com/photo-1544551763-46a8723ba3f9?q=80&w=2500&auto=format&fit=crop", // Boat
  };
</script>

<main class="w-full bg-white">
  <Hero image={images.hero} />
  
  <IntroText />
  
  <ProjectFull 
    client="Fagerhult"
    services="Communication Design + Communication Strategy + Public Relations"
    title="Fagerhult brand launch Germany"
    image={images.fagerhult}
  />
  
  <ProjectSplit 
    left={{
      client: "Craft",
      services: "Brand Strategy + Brand Design + Communication Design",
      image: images.craft
    }}
    right={{
      client: "Crescent",
      services: "Brand Strategy + Brand Design + Insights",
      image: images.crescent
    }}
  />
  
  <ProjectFull 
    client="Snif"
    services="Packaging Design + Communication Design + Product Design"
    title="Snif Mini"
    image={images.snif}
    largeTextOverlay="ni_snif.mi"
    largeTextOverlayClass="text-red-500/80 mix-blend-multiply"
  />
  
  <QuoteSection />
  
  <ProjectFull 
    client="Nikon"
    services="Communication Production + Public Relations + Communication Strategy"
    title="#createyourlight"
    image={images.nikon}
    largeTextOverlay="Nikon"
    largeTextOverlayClass="text-black/80 italic"
  />
  
  <ProjectFull 
    client="Škoda"
    services="Public Relations + Communication Design + Communication Strategy"
    title="ŠKODA Cycling Team"
    image={images.skoda}
  />
  
  <ProjectSplit 
    left={{
      client: "Bebo Objects",
      services: "Product Design + Communication Design + Brand Design",
      image: images.bebo
    }}
    right={{
      client: "Head",
      services: "Communication Production + Public Relations + Communication Design",
      image: images.head
    }}
  />
  
  <ProjectFull 
    client="Sturegallerian"
    services="Brand Design + Digital Development + Digital Design"
    title="A lifestyle destination with an international atmosphere"
    image={images.sture}
    largeTextOverlay="STURE<br>GALLERIAN"
    largeTextOverlayClass="text-white/30"
  />
  
  <ProjectFull 
    client="X Shore"
    services="Communication Design + Public Relations + Brand Strategy"
    title="Global launch of the X Shore 1"
    image={images.xshore}
  />
  
  <Footer />
</main>

