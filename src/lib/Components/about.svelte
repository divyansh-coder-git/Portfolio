<script lang="ts">
  import cover_img from "$lib/assets/img1.png";
  // import resume from "$lib/assets/resume.pdf";

  import Typed from "typed.js";

  // Define the custom Svelte action
  function typingEffect(node: HTMLElement) {
    const typed = new Typed(node, {
      strings: ["making Websites", "learning Machine Learning", "Exploring Data Science", "Creating usefull projects"],
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
  class="text-[#E4E8EF] min-h-screen px-[12%] w-full relative flex items-center justify-center snap-start"
>
  <div class="container flex items-center justify-center  mt-8 gap-5 sm:gap-40 flex-col sm:flex-row">
    <img class="w-[45vw] sm:w-[30vw]" src={cover_img} alt="CoverImage" />

    <div
      class="info-box flex flex-col text-center items-center gap-6 justify-center"
    >
      <div class="text flex flex-col gap-4 sm:gap-8">
        <h1 class="text-3xl lg:text-6xl text-[#E4E8EF] font-semibold text-nowrap">Divyansh Pandey</h1>
        <span class="text-xl sm:text-2xl text-[#ccd6f6] sm:text-nowrap">Electrical Engineering Student @ NIT Silchar</span>
        <h2 class="text-[1rem] sm:text-[2rem]">
          I love <span class="text-[#60a5fa]" use:typingEffect></span>
        </h2>
        <span class="text-[0.9rem] sm:text-[1.2rem] text-[#8892b0]">Passionate about Machine Learning, Web Development and building practical projects that solve real problems.</span>
      </div>

      <div class="btn-grp flex gap-2 sm:gap-4">
        <a
          href="/resume.pdf"
          target="_blank"
          rel="noopener noreferrer"
          class="rounded-[3rem] text-xs sm:text-base py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-white hover:text-black"
          >Download CV</a
        >
        <a
          href="#projects"
          class="rounded-[3rem] text-xs sm:text-base py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-white hover:text-black"
          >View Projects</a
        >
      </div>

      <div class="socials flex gap-4 sm:gap-8 text-[1.5rem] sm:text-[2.5rem]">
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
    cursor: pointer;
    transition: 0.2s ease-in-out;
  }

  div i:hover {
    transform: scale(1.1);
    color: #38bdf8;
  }
</style>
