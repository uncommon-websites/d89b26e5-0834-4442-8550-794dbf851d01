<script>
  import Header from './Header.svelte';
</script>

<section class="relative h-screen w-full overflow-hidden bg-gray-900 text-white">
  <!-- Background Image -->
  <div class="absolute inset-0 z-0">
    <img 
      src="https://images.unsplash.com/photo-1537462713505-a1ceac92ad28?q=80&w=2560&auto=format&fit=crop" 
      alt="Industrial Welding" 
      class="h-full w-full object-cover opacity-60"
    />
    <div class="absolute inset-0 bg-gradient-to-b from-black/30 via-transparent to-black/60"></div>
    <div class="absolute inset-0 bg-orange-900/20 mix-blend-overlay"></div>
  </div>

  <!-- Content -->
  <div class="relative z-10 flex h-full flex-col justify-between px-6 py-6 md:px-12">
    <Header />

    <div class="mb-20 max-w-4xl">
      <h1 class="font-sans text-5xl font-medium leading-tight tracking-tight md:text-7xl lg:text-8xl">
        Forging the <br />
        next industrial <br />
        revolution
      </h1>
      <div class="mt-8 max-w-md">
        <p class="text-lg font-light text-gray-200 md:text-xl">
          Making Western manufacturing competitive through industrial intelligence
        </p>
      </div>
    </div>

    <div class="flex items-center gap-2 text-xs font-medium tracking-widest text-gray-300 uppercase">
      <div class="h-2 w-2 rounded-full border border-current"></div>
      Scroll and Discover
    </div>
  </div>
</section>
