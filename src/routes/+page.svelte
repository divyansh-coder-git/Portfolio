<script lang="ts">
  import Navbar from "$lib/Components/navbar.svelte";
  import About from "$lib/Components/about.svelte";
  import Experience from "$lib/Components/experience.svelte";
  import Projects from "$lib/Components/projects.svelte";
  import Contacts from "$lib/Components/contact.svelte";
</script>

<div class="scrollbar-track-white scrollbar-thumb-black">
  <Navbar />
  <About />
  <Experience />
  <Projects />
  <Contacts />
</div>

<style>
  div {
    padding: 0;
    margin: 0;
    scroll-snap-type: mandatory;
    background: linear-gradient(135deg, #0f172a, #111827, #1e293b);
  }
</style>
