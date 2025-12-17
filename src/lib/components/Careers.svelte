<script>
  const jobs = [
    { title: 'Edge AI Engineer', category: 'TECH - ZURICH' },
    { title: 'Forward Deployed Engineer', category: 'TECH - ZURICH' },
    { title: 'AI Robotics Engineer', category: 'TECH - ZURICH' },
    { title: 'Product Growth Associate', category: 'PRODUCT - ZURICH' },
    { title: 'Head of Marketing', category: 'BUSINESS - ZURICH' },
    { title: 'People & Organizational Excellence Lead', category: 'OPERATIONS - ZURICH' }
  ];
</script>

<section class="bg-[#080C14] px-6 py-24 text-white md:px-12 md:py-32">
  <div class="mx-auto max-w-7xl">
    <div class="mb-24 flex flex-col justify-between gap-12 lg:flex-row lg:items-end">
      <h2 class="text-6xl font-medium tracking-tight md:text-7xl lg:text-8xl">You in?</h2>
      <div class="max-w-xl text-xl leading-relaxed text-gray-300 md:text-2xl">
        Zero passengers, everyone drives. <br />
        If you've been called arrogant, obsessive, or unmanageable - welcome to our Zurich HQ.
      </div>
    </div>

    <div class="grid grid-cols-1 gap-x-12 gap-y-0 md:grid-cols-2">
      {#each jobs as job}
        <a href="#" class="group flex items-center justify-between border-b border-gray-700 py-8 transition-colors hover:border-white">
          <div>
            <h3 class="text-xl font-medium text-white md:text-2xl">{job.title}</h3>
            <p class="mt-2 text-xs font-medium tracking-widest text-gray-500 uppercase">{job.category}</p>
          </div>
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-gray-500 transition-transform duration-300 group-hover:-translate-y-1 group-hover:translate-x-1 group-hover:text-white">
            <path d="M7 17L17 7M17 7H7M17 7V17" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </a>
      {/each}
    </div>
  </div>
</section>
