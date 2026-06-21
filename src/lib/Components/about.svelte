<script lang="ts">
  import cover_img from "$lib/assets/github-3.png";

  import Typed from "typed.js";

  // Define the custom Svelte action
  function typingEffect(node: HTMLElement) {
    const typed = new Typed(node, {
      strings: ["a Web Developer", "a ML Enthusiast", "an Aspiring Engineer"],
      typeSpeed: 50,
      backSpeed: 30,
      loop: true,
    });

    return {
      destroy() {
        typed.destroy();
      },
    };
  }
</script>

<div
  id="about"
  class="min-h-screen px-[12%] w-full relative flex items-center justify-center snap-start"
>
  <div class="container flex items-center justify-center gap-40">
    <img class="w-[30vw]" src={cover_img} alt="CoverImage" />

    <div
      class="info-box flex flex-col text-center items-center justify-center gap-6"
    >
      <div class="text">
        <h3 class="text-[1.8rem] font-medium opacity-80">Hi, I'm</h3>
        <h1 class="text-[4rem] font-semibold text-nowrap">Divyansh Pandey</h1>
        <h2 class="text-[2rem]">
          I'm <span class="text-purple-700" use:typingEffect></span>
        </h2>
      </div>

      <div class="btn-grp flex gap-4">
        <a
          href="https://google.com"
          class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
          >Download CV</a
        >
        <a
          href="#contact"
          class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
          >Contact</a
        >
      </div>

      <div class="socials flex gap-8">
        <a href="https://github.com/divyansh-coder-git" target="_blank" aria-label="SocialLinks"
          ><i class="fa-brands fa-github"></i></a
        >
        <a href="https://www.linkedin.com/in/divyansh-pandey-6180482a9/" target="_blank" aria-label="SocialLinks"
          ><i class="fa-brands fa-linkedin"></i></a
        >
        <a href="https://instagram.com/divyansh_coder" target="_blank" aria-label="SocialLinks"
          ><i class="fa-brands fa-instagram"></i></a
        >
      </div>
    </div>
  </div>
</div>

<style>
  div i {
    font-size: 2.5rem;
    cursor: pointer;
    transition: 0.2s ease-in-out;
  }

  div i:hover {
    transform: scale(1.1);
  }
</style>
