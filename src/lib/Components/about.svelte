<script lang="ts">
  import cover_img from "$lib/assets/img1.png";
  import Download from "@lucide/svelte/icons/download";
  import Arrowupright from "@lucide/svelte/icons/move-up-right";
  // import resume from "$lib/assets/resume.pdf";

  import Typed from "typed.js";

  // Define the custom Svelte action
  function typingEffect(node: HTMLElement) {
    const typed = new Typed(node, {
      strings: [
        "building good UIs.",
        "developing scalable tools.",
        "solving complex logic.",
      ],
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
  class="text-(--primary-text-color) min-h-screen px-[12%] pt-5 w-full relative flex items-center justify-center snap-start"
>
  <div
    class="container flex items-center justify-center mt-8 gap-5 lg:gap-40 flex-col lg:flex-row"
  >
    <img class="w-[45vw] lg:w-[30vw]" src={cover_img} alt="CoverImage" />

    <div
      class="info-box flex flex-col text-center items-center gap-6 justify-center"
    >
      <div class="text flex flex-col gap-4 lg:gap-8">
        <h1
          class="text-3xl lg:text-6xl text-(--primary-text-color) font-semibold text-nowrap"
        >
          Divyansh Pandey
        </h1>

        <span class="text-xl lg:text-2xl text-[#ccd6f6] lg:text-nowrap"
          >Electrical Engineering Student @ NIT Silchar</span
        >
        <h2 class="text-[1rem] lg:text-[2rem]">
          I love <span class="text-[#60a5fa]" use:typingEffect></span>
        </h2>
        <span class="text-[0.9rem] lg:text-[1.2rem] text-(--description-text-color)"
          >I enjoy building full-stack web applications, experimenting with
          machine learning, and turning ideas into practical software that
          people can actually use.</span
        >
      </div>

      <div class="btn-grp flex gap-2 lg:gap-4">
        <a
          // eslint-disable-next-line svelte/no-navigation-without-resolve
          href="/resume.pdf"
          target="_blank"
          rel="noopener noreferrer"
          class="group flex gap-2 items-center rounded-[3rem] text-xs lg:text-base py-2 px-6 cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 bg-linear-to-r from-[#4F8DFF] to-[#3B82F6] active:scale-95 hover:-translate-y-0.5"
          ><Download class="w-5 h-5 transition-transform duration-200 font-bold group-hover:translate-y-0.5"/>Download CV</a
        >
        <a
          href="#projects"
          class="group flex gap-2 items-center rounded-[3rem] text-xs lg:text-base py-2 px-6 border border-[#4f8dff] cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 active:scale-95 hover:-translate-y-0.5"
          >
          <Arrowupright  class="h-4 w-4 transition-transform duration-300 ease-out group-hover:-translate-y-0.5 group-hover:translate-x-0.5 group-hover:scale-125"/>

          View Projects</a
        >
      </div>

      <div class="socials flex gap-4 lg:gap-8 text-[1.5rem] lg:text-[2.5rem]">
        <a
          href="https://github.com/divyansh-coder-git"
          target="_blank"
          aria-label="SocialLinks"><i class="fa-brands fa-github"></i></a
        >
        <a
          href="https://www.linkedin.com/in/divyansh-pandey-nits/"
          target="_blank"
          aria-label="SocialLinks"><i class="fa-brands fa-linkedin"></i></a
        >
        <a
          href="https://instagram.com/divyansh._.pandey__/"
          target="_blank"
          aria-label="SocialLinks"><i class="fa-brands fa-instagram"></i></a
        >
      </div>
    </div>
  </div>
</div>

<style>
  div i {
    cursor: pointer;
    transition: 0.2s ease-in-out;
  }

  div i:hover {
    transform: scale(1.1);
    color: #38bdf8;
  }
</style>
