<script>
  import Header from './Header.svelte';
</script>

<section class="relative h-screen w-full overflow-hidden bg-gray-900 text-white">
  <!-- Background Image -->
  <div class="absolute inset-0 z-0">
    <img 
      src="https://images.unsplash.com/photo-1625246333195-78d9c38ad449?q=80&w=2560&auto=format&fit=crop" 
      alt="Heavy Mining Equipment" 
      class="h-full w-full object-cover opacity-50"
    />
    <div class="absolute inset-0 bg-gradient-to-b from-black/40 via-transparent to-black/70"></div>
    <div class="absolute inset-0 bg-gray-900/30 mix-blend-overlay"></div>
  </div>

  <!-- Content -->
  <div class="relative z-10 flex h-full flex-col justify-between px-6 py-6 md:px-12">
    <Header />

    <div class="mb-20 max-w-4xl">
      <h1 class="font-sans text-5xl font-medium leading-tight tracking-tight md:text-7xl lg:text-8xl">
        Autonomous <br />
        heavy equipment <br />
        for continuous operation
      </h1>
      <div class="mt-8 max-w-md">
        <p class="text-lg font-light text-gray-200 md:text-xl">
          Retrofitting mining and construction fleets with plug-and-play AI for 24/7 safe productivity
        </p>
      </div>
    </div>

    <div class="flex items-center gap-2 text-xs font-medium tracking-widest text-gray-300 uppercase">
      <div class="h-2 w-2 rounded-full border border-current"></div>
      Scroll and Discover
    </div>
  </div>
</section>
