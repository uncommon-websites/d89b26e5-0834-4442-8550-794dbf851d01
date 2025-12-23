<script lang="ts">
  import { onMount } from 'svelte';

  let activeSection = 'making-kind';

  const sections = [
    { id: 'making-kind', number: '01', title: 'The Challenge' },
    { id: 'industrial-intelligence', number: '02', title: 'The Solution' },
    { id: 'why-now', number: '03', title: 'The Scale' }
  ];

  function handleScroll() {
    const sectionElements = sections.map(s => document.getElementById(s.id));
    const scrollPosition = window.scrollY + window.innerHeight / 3;

    for (const section of sectionElements) {
      if (section && section.offsetTop <= scrollPosition && (section.offsetTop + section.offsetHeight) > scrollPosition) {
        activeSection = section.id;
      }
    }
  }

  function scrollTo(id: string) {
    const el = document.getElementById(id);
    if (el) {
      el.scrollIntoView({ behavior: 'smooth' });
    }
  }
</script>

<svelte:window on:scroll={handleScroll} />

<section class="bg-[#E5E7EB] text-gray-900 w-full">
  <div class="mx-auto flex max-w-7xl flex-col px-6 py-24 md:flex-row md:px-12 md:py-32">
    
    <!-- Sticky Sidebar -->
    <div class="mb-12 w-full md:mb-0 md:w-1/3 lg:w-1/4">
      <div class="sticky top-32 flex flex-col gap-4 border-l border-gray-300 py-2">
        {#each sections as section}
          <button 
            class="group flex items-center justify-between pl-4 text-left text-sm font-medium transition-colors hover:text-black
            {activeSection === section.id ? 'text-black' : 'text-gray-500'}"
            on:click={() => scrollTo(section.id)}
          >
            <span class="flex items-center gap-3">
              <span class="text-xs font-mono">{section.number}</span>
              {section.title}
            </span>
            {#if activeSection === section.id}
              <div class="h-1.5 w-1.5 bg-primary-600"></div>
            {/if}
          </button>
        {/each}
      </div>
    </div>

    <!-- Content -->
    <div class="w-full md:w-2/3 lg:w-3/4 md:pl-12 lg:pl-24">
      
      <!-- Section 1 -->
      <div id="making-kind" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">The Challenge</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">Critical infrastructure depends on earthmoving.</em> Every mine, every construction site, every piece of planetary-scale infrastructure begins with moving earth. Excavators, bulldozers, loaders—these machines shape the physical world, extracting resources and building the foundations of civilization. Yet the industry faces an existential crisis: a severe labor shortage colliding with relentless demand for productivity.
          </p>
          <p>
            <em class="text-gray-500">Human operators face impossible conditions.</em> Mining and construction sites are among the most dangerous work environments on Earth. Operators work in extreme weather, navigate hazardous terrain, and face constant risk of injury or death. Heat, dust, isolation, and the physical toll of operating heavy machinery for extended shifts make recruitment difficult and retention nearly impossible. The workforce is aging, and younger generations are choosing safer, more appealing careers.
          </p>
          <p>
            <em class="text-gray-500">Productivity stops when humans must.</em> Equipment sits idle during shift changes, overnight, and in conditions too dangerous for human operation. Mining operations lose millions in downtime. Construction projects fall behind schedule. The $180 billion earthmoving market is constrained not by demand or capital, but by the fundamental limitation of human endurance and safety requirements. The machines are capable of 24/7 operation—but only if we can remove humans from harm's way while maintaining control.
          </p>
        </div>
      </div>

      <!-- Section 2 -->
      <div id="industrial-intelligence" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">The Solution</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">Retrofit any equipment, any age, any brand.</em> AIM's breakthrough is universality. Unlike competitors who require new equipment purchases or brand-specific integrations, our plug-and-play AI system retrofits existing fleets in 24 hours. Excavators, bulldozers, loaders, compactors—if it moves earth, we can make it autonomous. The same LiDAR, cameras, and sensor technology that powers self-driving cars now operates in the harshest environments on Earth, creating real-time 3D maps and navigating terrain that would challenge even experienced human operators.
          </p>
          <p>
            <em class="text-gray-500">Autonomous operation, human oversight.</em> Our systems don't replace human expertise—they amplify it. Operators transition from cab seats to remote control centers, managing multiple machines simultaneously through intuitive interfaces. They upskill into site planning, fleet optimization, and data analytics roles. Real-time KPI data flows continuously, enabling short-interval control strategies and daily performance tracking. When conditions become too dangerous for humans—extreme weather, unstable ground, toxic environments—the machines continue working autonomously while humans remain safe.
          </p>
          <p>
            <em class="text-gray-500">Fully insured, fully validated.</em> AIM-enabled machines are fully insured for autonomous operation by a global insurance company—a validation that our safety systems meet the highest standards. We've deployed at Fortune 500 mining operations including Minerals Technologies Inc., proving our technology in real-world conditions. Zero-entry sites eliminate hazard exposure entirely. Continuous operation means no shift changes, no fatigue-related errors, no weather delays. The result: maximum safety, maximum productivity, and a clear path to scaling autonomous fleets across the $180 billion earthmoving market.
          </p>
        </div>
      </div>

      <!-- Section 3 -->
      <div id="why-now" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">The Scale</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">$180 billion market, proven deployment model.</em> We're starting with mining fleets where the value proposition is clearest: continuous operation in dangerous conditions with immediate ROI. But the addressable market extends across the entire earthmoving industry—construction, infrastructure development, land reclamation. Every bulldozer, every excavator, every loader represents an opportunity to deploy our retrofit technology. With 24-hour installation time and compatibility with any equipment brand, we can scale rapidly without the constraints of manufacturing new machines.
          </p>
          <p>
            <em class="text-gray-500">World-class team and backing.</em> Our engineering team brings experience from Google, Waymo, SpaceX, Tesla, and leading AI research institutions. We've assembled an advisory board spanning AI pioneers (Transformer co-inventor Jakob Uszkoreit, Microsoft CSO Eric Horvitz), military leadership (Lt. Gen. H.R. McMaster), and mining operations experts with 40+ years of field experience. In June 2025, we raised $50 million from Khosla Ventures, General Catalyst, DCVC, and other top-tier investors who understand the magnitude of this opportunity.
          </p>
          <p>
            <em class="text-gray-500">Mission-driven, execution-focused.</em> We're not building autonomous equipment as a technology demonstration. We're terraforming this planet—reversing the negative effects of climate change by enabling the construction of planetary-scale infrastructure. We're automating the world to make jobs safe and productive, eliminating hazards while upskilling workers into higher-value roles. This is the next industrial revolution, and we're deploying it today across operations in the United States, Australia, Africa, and Europe. Thousands of autonomous machines. Continuous safe operation. The future of earthmoving is here.
          </p>
        </div>
      </div>

    </div>
  </div>
</section>
