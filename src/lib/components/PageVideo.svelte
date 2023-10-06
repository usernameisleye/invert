<script>
  import { PlayCircle } from "lucide-svelte"
  let isPlaying = false
</script>

<!-- In construction... -->
<div class="md:w-3/4 relative mx-auto">
  {#if isPlaying}
    <iframe
      frameborder="0"
      allowfullscreen={true}
      title="Video"
      width="640"
      height="360"
      class="w-full h-full flex border-none"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      src="https://www.youtube.com/embed/jfKfPfyJRdk?controls=1&rel=0&playsinline=0&modestbranding=0&autoplay=0&enablejsapi=1&origin=https%3A%2F%2Fstrikex.com&widgetid=1"
    />
  {:else}
    <button
      tabindex="0"
      aria-label="Play Video"
      on:click={() => (isPlaying = !isPlaying)}
      class="z-10 transition-all absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 py-4 px-8 w-max rounded-full bg-slate-500 shadow-lg flex items-center gap-2 hover:scale-95"
    >
      <PlayCircle />
      Play Video
    </button>
    <!-- svelte-ignore a11y-media-has-caption -->
    <video
      loop
      autoplay
      playsinline
      disablepictureinpicture
      class="h-full w-full flex border-none rounded-lg"
    >
      <source type="video/mp4" src="/assets/video_3.mp4" />
      <p>Sorry your browser does not support HTML5 videos</p>
    </video>
  {/if}
</div>

<!-- https://youtu.be/Y-x0efG1seA -->
<!-- https://youtu.be/jfKfPfyJRdk -->
