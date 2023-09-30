<script lang="ts">
  import { fly } from "svelte/transition"
  import { Logo } from "."
  import { page } from "$app/stores"
  import { Menu, X } from "lucide-svelte"

  let isOpen: boolean = false

  const links = [
    {
      href: "/partners",
      pageName: "Partners & Integrations"
    },
    {
      href: "/about",
      pageName: "About"
    },
    {
      href: "/contact-us",
      pageName: "Contact Us"
    }
  ]
</script>

<div>
  <nav class="fixed top-0 inset-x-0 z-30 h-fit p-6 backdrop-blur">
    <div class="max-w-7xl mx-auto flex justify-between items-center gap-4">
      <a href="/">
        <Logo />
      </a>

      <ul class="hidden lg:flex items-center gap-6 h-auto">
        {#each links as { href, pageName } (href)}
          <a {href} class="relative">
            <li
              aria-label="page-links"
              class="transition-all after:absolute after:bottom-0 after:left-0 after:h-[2px] after:w-full after:origin-bottom-left after:origin-right after:ease-spring after:scale-x-0 after:bg-foreground after:opacity-80 after:transition-transform after:duration-500 after:content-[''] hover:text-foreground hover:after:origin-bottom-left hover:after:scale-x-100"
            >
              {pageName}
            </li>
          </a>
        {/each}
      </ul>

      <button
        aria-label="Open menu"
        class="menu block lg:hidden outline-none"
        on:click={() => (isOpen = !isOpen)}
      >
        {#if isOpen}
          <div in:fly={{ y: -10 }}>
            <X />
            <span>Close</span>
          </div>
        {:else}
          <div in:fly={{ y: 10 }}>
            <Menu />
            <span>Menu</span>
          </div>
        {/if}
      </button>
    </div>
  </nav>

  <div class="block lg:hidden">
    <ul
      class="fixed inset-0 z-20 bg-slate-400 h-auto flex flex-col items-start justify-center gap-12 p-8 duration-300 {isOpen
        ? '-translate-y-0 opacity-100'
        : '-translate-y-full opacity-0'}"
    >
      {#each links as { href, pageName } (href)}
        <a {href} class="relative">
          <li
            aria-label="page-links"
            class="transition-all text-4xl font-medium {$page.url.pathname.startsWith(href)
              ? 'underline underline-offset-2'
              : null}"
          >
            {pageName}
          </li>
        </a>
      {/each}
    </ul>
  </div>
</div>

<style lang="postcss">
  .menu > * {
    @apply flex items-center gap-2;
  }
</style>
