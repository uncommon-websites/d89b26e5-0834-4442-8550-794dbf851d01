<section class="relative w-full bg-[#080C14] py-32 text-white overflow-hidden">
  <!-- Background Decorations (Subtle lines) -->
  <div class="absolute inset-0 opacity-15 pointer-events-none">
    <!-- Large Circle -->
    <div class="absolute left-1/2 top-1/2 h-[900px] w-[900px] -translate-x-1/2 -translate-y-1/2 rounded-full border border-dashed border-gray-500/50"></div>
    <!-- Smaller intersecting circles -->
    <div class="absolute left-[20%] bottom-[-100px] h-[500px] w-[500px] rounded-full border border-dashed border-gray-600/50"></div>
    <div class="absolute right-[20%] top-[-100px] h-[600px] w-[600px] rounded-full border border-dashed border-gray-600/50"></div>
    
    <!-- Grid lines -->
    <div class="absolute left-0 top-1/2 h-px w-full -translate-y-1/2 bg-gradient-to-r from-transparent via-gray-700/30 to-transparent"></div>
    <div class="absolute left-1/2 top-0 h-full w-px -translate-x-1/2 bg-gradient-to-b from-transparent via-gray-700/30 to-transparent"></div>
  </div>

  <div class="relative z-10 mx-auto flex max-w-7xl flex-col items-center px-6 md:px-12">
    <!-- Center Logo/Title -->
    <div class="mb-32 flex items-center gap-6 text-6xl font-medium tracking-tight md:text-7xl lg:text-8xl">
      <span class="opacity-100">Forg</span>
      <div class="relative flex items-center justify-center">
        <svg width="64" height="64" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="animate-pulse text-white">
          <path d="M12 2L15 9L22 12L15 15L12 22L9 15L2 12L9 9L12 2Z" fill="currentColor"/>
        </svg>
        <div class="absolute inset-0 blur-lg bg-white/20 rounded-full"></div>
      </div>
      <span>is</span>
    </div>

    <!-- Text Content -->
    <div class="grid w-full grid-cols-1 gap-12 md:grid-cols-2">
      <div></div> <!-- Spacer for left column -->
      <div class="space-y-10 text-lg leading-relaxed text-gray-300 md:text-xl font-light">
        <p>
          <strong class="text-white font-medium">Forgis is a company that creates tangible value</strong> for manufacturers via a one-stop platform powered by cutting-edge technologies.
        </p>
        <p>
          We're building a future where Western manufacturers and engineers are supercharged by industrial intelligence to design, automate, and optimized production with unprecedented power and efficiency.
        </p>
      </div>
    </div>
    
    <!-- Bottom technical markers -->
    <div class="absolute bottom-8 left-8 text-[9px] font-mono text-gray-600 tracking-widest opacity-60">
      002.448.17<br>
      14.04.29.42
    </div>
  </div>
</section>
