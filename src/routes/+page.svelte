<script lang="ts">
  import { PageVideo, Button } from "$lib/components"
</script>

<div class="relative">
  <div class="container py-20">
    <header class="flex flex-col justify-center items-center">
      <div class="text-center max-w-5xl transition">
        <h1 class="leading-tight font-semibold text-5xl tracking-tight md:text-7xl md:font-bold">
          Curating the future of
          <span
            class="bg-gradient-to-b from-slate-300 to-slate-400 bg-clip-text text-transparent w-0"
          >
            tokenisation.
          </span>
        </h1>
      </div>

      <p
        class="max-w-5xl font-medium text-center text-base text-muted-foreground my-4 leading-7 md:leading-8 md:text-lg"
      >
        Our ground-breaking investments and partnerships are taking off soon. Learn how this
        partnership marks a significant milestone in our journey to bring
        <span class="text-slate-400">tokenisation</span>
        technology to the securities markets and addresses the critical questions surrounding the adoption
        of blockchain applications in regulated financial environments.
      </p>

      <div class="p-8 overflow-hidden">
        <PageVideo />
      </div>
    </header>
  </div>

  <section class="container my-20 md:max-w-7xl">
    <div class="flex items-center flex-col md:flex-row justify-between gap-12">
      <div class="grid gap-6 justify-center text-center md:text-left">
        <h3 class="font-medium text-xl tracking-wide text-muted-foreground">
          Pioneering for the people
        </h3>
        <h3
          class="text-slate-400 leading-[3.5rem] text-4xl font-medium md:text-5xl md:font-semibold md:max-w-md"
        >
          Evolution in blockchain.
        </h3>
        <p class="md:max-w-lg leading-8 text-lg">
          Here at Invert, our mission is to develop truly revolutionary software. Through innovation
          in blockchain technologies, we are building a far reaching, efficient & disruptive
          ecosystem that will transform financial technology.
        </p>

        <div>
          <Button class="rounded-full transition-all">
            <a href="/about" class="capitalize leading-5 font-semibold w-fit">
              Learn more about us
            </a>
          </Button>
        </div>
      </div>

      <div class="grow transition-all">
        <img
          alt="Vector"
          src="/assets/images/vector_1.svg"
          class="w-full h-full object-cover select-none"
        />
      </div>
    </div>
  </section>

  <section class="bg-muted container my-20">
    <div class="md:max-w-5xl mx-auto">
      <div class="flex flex-col justify-center items-center gap-3 text-center">
        <h3 class="font-medium text-xl tracking-wide text-muted-foreground">Building the future</h3>
        <h3
          class="text-slate-400 leading-[3.5rem] text-4xl font-medium md:text-5xl md:font-semibold md:max-w-md"
        >
          Opportunity in blockchain
        </h3>
        <p class="md:max-w-lg leading-8 text-lg">
          Blockchain technology is now entering the mainstream as innovation begins to open doors to
          unlimited possibilities. At StrikeX we recognise its potential to profoundly transform the
          way businesses, governments & financial markets operate.
        </p>
      </div>

      <div class="">
        <div class="">
          <p class="text-xl">The global blockchain market is projected to grow from $7.18 billion in 2022 to $163.83 billion by 2029, at a CAGR of 56.3%</p>
          <p class="text-xs uppercase">FORTUNEBUSINESSINSIGHT.COM</p>
        </div>
        
        <div class="">
          <img src="" alt="">
        </div>
      </div>

      <div class="" />
    </div>
  </section>
</div>
