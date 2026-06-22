<script lang="ts">
  import Navbar from "$lib/Components/navbar.svelte";
  import About from "$lib/Components/about.svelte";
  import Experience from "$lib/Components/experience.svelte";
  import Projects from "$lib/Components/projects.svelte";
  import Contacts from "$lib/Components/contact.svelte";

  let mouseX = $state(0);
  let mouseY = $state(0);

  function handleMouseMove(e: MouseEvent) {
    mouseX = e.clientX;
    mouseY = e.clientY;
  }
</script>

<svelte:window onmousemove={handleMouseMove} />

<div
  class="fixed inset-0 pointer-events-none z-0"
  style={`background: radial-gradient(
		600px at ${mouseX}px ${mouseY}px,
		rgba(29, 78, 216, 0.15),
		transparent 80%
	)`}
></div>
<div class="bg-[#0a192f]">
  <div
    class="relative z-1000 main-div scrollbar-track-white scrollbar-thumb-black"
  >
    <Navbar />
    <About />
    <Experience />
    <Projects />
    <Contacts />
  </div>
</div>

<style>
  :global(html) {
    /* font-family: "Inter", sans-serif; */
    font-family: "Pliant", sans-serif;
    font-optical-sizing: auto;
  }
</style>
