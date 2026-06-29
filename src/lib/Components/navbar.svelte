<script lang="ts">
  let isOpen = $state(false);

  function clickOutside(node: HTMLElement, callback: () => void) {
    const handleClick = (event: MouseEvent) => {
      const target = event.target as HTMLElement;
      
      if (node && !node.contains(target)) {
        callback();
      }
    };

    document.addEventListener('click', handleClick, true);

    return {
      destroy() {
        document.removeEventListener('click', handleClick, true);
      }
    };
  }
  const toggleMenu = () => isOpen = !isOpen;
  const closeMenu = () => isOpen = false;
</script>

<div
  use:clickOutside={closeMenu}
  class="nav-div text-black flex gap-20 rounded-full items-center px-6 py-2 top-4 left-1/2 fixed -translate-x-1/2 bg-white/60 w-fit justify-center backdrop-blur z-10"
>
  <h1
    class="text-[1.3em] cursor-pointer font-semibold text-nowrap transition-all ease-in-out duration-200 hover:scale-105"
  >
    <a href="#about">Divyansh Pandey</a>
  </h1>
  <ul class="nav-ul {isOpen ? 'active' : 'no-active'} flex gap-3 md:gap-8">
    <li>
      <a href="#about">About</a>
    </li>
    <hr />
    <li>
      <a href="#projects">Projects</a>
    </li>
    <hr />
    <li>
      <a href="#experience">Skills</a>
    </li>
    <hr />
    <li>
      <a href="#contact">Contacts</a>
    </li>
  </ul>

  <button
    onclick={toggleMenu}
    aria-label="ToggleButton"
    class="block md:hidden"
  >
    <i class="fa-solid fa-bars"></i>
  </button>

  <!-- <a href="https://github.com/divyansh-coder-git" target="_blank"><button
    class="flex items-center justify-center gap-2 px-6 py-1 rounded-[3rem] text-black bg-slate-200 border border-slate-700 hover:bg-black hover:text-white text-nowrap font-medium text-[1rem] cursor-pointer transition-all ease-in-out durartion-300 hover:scale-105"
    ><img
      src={github_icon}
      alt="Github"
      class="relative w-8 p-0 m-0"
    />Github</button></a> -->

  <a
    class="git-btn"
    href="https://github.com/divyansh-coder-git"
    target="_blank"
    ><button
      class="flex items-center justify-center gap-2 px-4 py-1 rounded-[3rem] text-black bg-slate-200 border border-slate-700 hover:bg-black hover:text-white text-nowrap font-medium text-[1rem] cursor-pointer transition-all ease-in-out durartion-300 hover:scale-105"
      ><i class="fa-brands fa-github"></i>Github</button
    ></a
  >
</div>

<style>
  *:not(i) {
    font-family: "Poppins", sans-serif;
  }
  li a {
    position: relative;
    color: black;
    font-weight: 300;
  }

  li a::before {
    position: absolute;
    content: "";
    width: 0px;
    left: 0px;
    height: 3px;
    top: 19px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: black;
  }

  .nav-div hr {
    display: none;
  }

  li a:hover::before {
    width: 100%;
  }

  a button i {
    font-size: 25px;
    height: auto;
  }

  @media (max-width: 640px) {
    .nav-div {
      width: 90vw;
      justify-content: space-between;
    }

    .nav-div hr {
      display: block;
      padding: 0px;
    }

    .git-btn {
      display: none;
    }

    .nav-ul {
      position: absolute;
      top: 100%;
      left: 0%;
      width: 100%;
      display: flex;
      flex-direction: column;
      text-align: center;
      background-color: rgba(255, 255, 255, 0.6);
      border-radius: 1.5rem;
      padding: 0.5rem 0;
      margin-top: 0.5rem;
      display: none;
    }

    .nav-ul.active {
      display: flex;
    }
  }
</style>
