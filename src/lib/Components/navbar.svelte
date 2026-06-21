<script lang="ts">
  import github_icon from "$lib/assets/github-3.png";
</script>

<div
  class="text-white flex gap-20 rounded-full items-center px-6 py-2 top-4 left-1/2 fixed -translate-x-1/2 bg-black/80 w-fit justify-center backdrop-blur z-10"
>
  <h1
    class="text-[1.3em] cursor-pointer font-semibold text-nowrap transition-all ease-in-out duration-200 hover:scale-105"
  >
    <a href="#about">Divyansh Pandey</a>
  </h1>
  <ul class="flex gap-8">
    <li>
      <a href="#about">About</a>
    </li>
    <li>
      <a href="#projects">Projects</a>
    </li>
    <li>
      <a href="#experience">Skills</a>
    </li>
    <li>
      <a href="#contact">Contacts</a>
    </li>
  </ul>

  <div class="hidden">
    <i class="fa-solid fa-bars"></i>
  </div>

  <a href="https://github.com/divyansh-coder-git" target="_blank"><button
    class="flex items-center justify-center gap-2 px-6 py-1 rounded-[3rem] text-black bg-slate-200 border border-slate-700 hover:bg-slate-600 hover:text-white text-nowrap font-medium text-[1rem] cursor-pointer transition-all ease-in-out durartion-300 hover:scale-105"
    ><img
      src={github_icon}
      alt="Github"
      class="relative w-8 p-0 m-0"
    />Github</button></a>

</div>

<style>
  * {
    font-family: "Poppins", sans-serif;
  }
  li a {
    position: relative;
    color: white;
    font-weight: 300;
  }

  li a::before {
    position: absolute;
    content: "";
    width: 0px;
    left: 0px;
    height: 3px;
    top: 27px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: white;
  }

  li a:hover::before {
    width: 100%;
  }
</style>
