<script lang="ts">
  import { onMount } from 'svelte';

  let activeSection = 'making-kind';

  const sections = [
    { id: 'making-kind', number: '01', title: 'The Making Kind' },
    { id: 'industrial-intelligence', number: '02', title: 'Industrial intelligence' },
    { id: 'why-now', number: '03', title: 'Why now?' }
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
              <div class="h-1.5 w-1.5 bg-orange-500"></div>
            {/if}
          </button>
        {/each}
      </div>
    </div>

    <!-- Content -->
    <div class="w-full md:w-2/3 lg:w-3/4 md:pl-12 lg:pl-24">
      
      <!-- Section 1 -->
      <div id="making-kind" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">The Making Kind</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">We are makers.</em> What makes us human, what elevates us beyond all other forms of life is our ability to transform matter and knowledge into value - be it things or ideas - shaping experience into new inventions that make us and our lives better. Since the dawn of time, we've bent fire to our will, carved stone into tools, turned sound into language, and thoughts into technology. We don't just adapt and wait for the world to change; we forge the future with our own hands. Every spark, every structure, every idea is a declaration that we never stop becoming.
          </p>
          <p>
            <em class="text-gray-500">Creation becomes reality through production.</em> The very trait that makes us a super-species is also the engine behind every era, the force that turns imagination into substance, supplying the concepts and artifacts that define civilization. In the feudal age, society rested on those who controlled the land and the hands that work it, and the main purpose was survival: food, protection, stability. With the Industrial Revolution, humanity crossed into the capitalist stage, where control shifted to those who owned the means of production: the machines, the labour, the capital. From the forge to the factory, the West has carried the torch of progress.
          </p>
          <p>
            <em class="text-gray-500">The West is losing against the East.</em> Western companies are being challenged - and beaten - in critical industries of tomorrow. Renewables are the energy of the future, and they are mostly produced in Asia. Robotics is the next manufacturing, and over two-thirds of the market belong to the East. Rare earths, semiconductors, and batteries are the raw materials of innovation, and China controls the first link of every supply chain. Intelligence is the only strategic frontier where the game between the two sides of the world remains contended. For the last twenty years, everyone predicted an Asian century with China as its next hegemon. They may be right about the trajectory, but they are wrong about the ending. We are losing, yes, but we will not lose.
          </p>
        </div>
      </div>

      <!-- Section 2 -->
      <div id="industrial-intelligence" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">Industrial intelligence</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">Factories were built to produce, not to reason.</em> Designed as closed systems, machines operate in fragments: precise in motion, blind in coordination. Fragmented across vendors, rigid in design and frozen in time, PLCs, robots, sensors, and drives are fluent in their own language but don't speak to one another. The result is a brainless system: efficient in parts, inefficient as a whole. Data flows endlessly but meaning goes nowhere. Intelligence - the frontier on which East and West now compete - has yet to reach the factory floor. Downtime grows, throughput falls, and production is offshored for cheap labour enabling flexible automation. We have mastered the mechanics, but not the mind.
          </p>
          <p>
            <em class="text-gray-500">We are the intelligent layer for the real world.</em> We build the foundational software that brings physical intelligence into hardware, an AI-native orchestration infrastructure for the industrial space. Its platform runs causal AI agents on the edge, digital engineers that learn from data, make decisions and optimize production performance in real time, configuring and validating manufacturing lines, predicting failures, and guiding operators to act before downtime occurs. From one unified interface, Forgis connects machines, information, and logic, transforming disconnected automation into network of smart organisms: the brain of the factory.
          </p>
          <p>
            <em class="text-gray-500">Forgis unlocks the next industrial revolution,</em> a world where factories operate as plug-and-play systems: adaptive, collaborative, and self-optimizing. Each plant becomes part of a cognitive network linking demand, design, and production. Orders flow directly from digital marketplaces into the line, and AI agents interpret requirements, reconfigure machines, and adjust parameters in real time to manufacture different products on demand. Just-in-time, tailored manufacturing becomes the norm; mass production, with its waste, the exception. A shift in corporate strategy translates instantly into a shift in physical output: strategy becomes execution. Humans act as conductors, freed from routine troubleshooting, focusing on creation, quality, and innovation, while the factory runs in seamless orchestration below. Domestic fabrication regains its edge over offshoring; flexibility is no longer outsourced but embedded in the system itself. Downtime fades, inefficiency disappears, and carbon emission from transportation minimized. This is Industry 5.0, an era of modular, sustainable, and human-centered manufacturing, driven by Forgis industrial intelligence.
          </p>
        </div>
      </div>

      <!-- Section 3 -->
      <div id="why-now" class="mb-32 scroll-mt-32">
        <h2 class="mb-12 text-4xl font-medium md:text-5xl">Why now?</h2>
        <div class="space-y-8 text-lg leading-relaxed text-gray-800">
          <p>
            <em class="text-gray-500">Technology is converging.</em> For years, intelligent automation was out of reach: vision too unreliable, compute too slow, and integration too brittle. That has changed. AI agents can now reason, plan, and collaborate, while edge devices can host powerful GPUs and large language models that bring cognition directly to the shop floor, and multi-agent systems synchronize decision-making across machines. These breakthroughs point toward the next organic step in technology: physical AI.
          </p>
          <p>
            <em class="text-gray-500">Factories are back on the political map.</em> From American reshoring plans to Europe's industrial revival, the West is rediscovering the strategic power of making. Yet hardware - the foundation of that strength - is now commoditized and largely owned by Asia. Intelligence is now the all-in move of the United States, the pivot on which global hegemony is being played. Whoever masters industrial cognition will define the next era of production.
          </p>
          <p>
            <em class="text-gray-500">We are obsessed with the problem.</em> We like the challenge, thriving on decoding the intricate puzzle of industrial automation. We are intense, putting twice the speed, triple the time, every day. We get things done: high quantity at high quality, staying until it works right. We are hungry: we win, unafraid to step on the lines. We are not a family; we are comrades on a mission: to bring machine intelligence to Western factories.
          </p>
        </div>
      </div>

    </div>
  </div>
</section>
