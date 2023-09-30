<script>
  import "../app.css"
  import { Footer, Navbar } from "$lib/components"
</script>

<svelte:head>
  <title>Home - Invert</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Curating the future of tokenisation. Learn how this partnership marks a significant milestone in our journey to bring tokenisation technology to the securities markets and addresses the critical questions surrounding the adoption of blockchain applications in regulated financial environments. Pioneering for the people"
  />
</svelte:head>

<div class="pt-12">
  <Navbar />

  <main id="main-content" class="antialiased font-normal text-base pt-12">
    <slot />
  </main>

  <!-- <Footer /> -->
</div>
