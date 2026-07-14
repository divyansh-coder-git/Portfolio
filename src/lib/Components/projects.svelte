<script lang="ts">
  import project_img_1 from "$lib/assets/project1.png";
  import project_img_2 from "$lib/assets/project6.png";
  import project_img_3 from "$lib/assets/project5.png";

  import Livedemo from "@lucide/svelte/icons/square-arrow-out-up-right";

  import { onMount } from "svelte";

  onMount(() => {
    const cards = document.querySelectorAll(".reveal");
    console.log(cards);

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          console.log(entry.isIntersecting);
          if (entry.isIntersecting) {
            entry.target.classList.add("show");
            observer.unobserve(entry.target); // animate only once
          }
        });
      },
      {
        threshold: 0.2,
      },
    );

    cards.forEach((card) => observer.observe(card));
  });
</script>

<hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] border-none h-px snap-start"
/>

<!-- <hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] lg:bg-gray-200 border-none h-px snap-start"
/> -->

<div
  class="text-white min-h-screen flex flex-col scroll-smooth snap-center lg:justify-around px-5 lg:px-15"
>
  <!-- lg:mt-25 -->
  <!-- mt-5 -->
  <div class="m-0 p-0 h-12 w-full"></div>
  <h1
    class="text-4xl lg:text-5xl text-[#ccd6f6] font-semibold text-center lg:mb-3"
  >
    Recent <span class="text-(--secondary-theme-text-color)">Projects</span>
  </h1>
  <!-- lg:mb-12 -->

  <div
    class="grid grid-cols-1 lg:grid-cols-3 gap-4 lg:gap-8 px-5 py-7 lg:px-10 lg:py-0 mb-5"
  >
    <div class="reveal h-full" style="transition-delay: 0ms;">
      <div class="grid-card">
        <img src={project_img_1} alt="ProjectImg" />
        <div class="flex flex-col gap-2 lg:gap-4">
          <h3>Habit Tracker</h3>
          <span>Track your daily routines and build positive habits effortlessly.Stay consistent and reach your goals.</span>

          <div class="tech-stack">
            <span>Svelte</span>
            <span>TypeScript</span>
            <span>Tailwind</span>
          </div>
          <div class="flex gap-2 lg:gap-5 w-fit m-auto">
            <a
              href="https://habit-tracker-svelte.netlify.app/"
              target="_blank"
              aria-label="View live demo of habit tracker"
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 bg-linear-to-r from-[#4F8DFF] to-[#3B82F6] hover:-translate-y-1 active:scale-95"
                ><Livedemo class="w-4 h-4" />
                Live Demo</button
              ></a
            >
            <a
              href="https://github.com/divyansh-coder-git/habit-tracker-svelte"
              target="_blank"
              aria-label="View source code of habit tracker on Github."
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base border border-[#4f8dff] cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:-translate-y-1 active:scale-95"
                ><i class="fa-brands fa-github"></i>Github Repo</button
              ></a
            >
          </div>
        </div>
      </div>
    </div>
    <div class="reveal" style="transition-delay: 75ms;">
      <div class="grid-card h-full">
        <img src={project_img_2} alt="ProjectImg" />
        <div class="flex flex-col gap-2 lg:gap-4">
          <h3>Hostel Allocation System</h3>
          <span
            >Automated room assignment from Excel-based participant and room
            data.</span
          >
          <div class="tech-stack">
            <span>Svelte</span>
            <span>TypeScript</span>
            <span>Tailwind</span>
          </div>
          <div class="flex gap-2 lg:gap-5 w-fit m-auto">
            <a
              href="https://hostel-allotment.netlify.app/"
              target="_blank"
              aria-label="View Live Demo of Hostel Allotment system."
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 bg-linear-to-r from-[#4F8DFF] to-[#3B82F6] hover:-translate-y-1 active:scale-95"
                ><Livedemo class="w-4 h-4" />
                Live Demo</button
              ></a
            >
            <a
              href="https://github.com/divyansh-coder-git/hackathon-hostel-allotment-system"
              target="_blank"
              aria-label="View source code of hostel allotment on github."
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base border border-[#4f8dff] cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:-translate-y-1 active:scale-95"
                ><i class="fa-brands fa-github"></i>Github Repo</button
              ></a
            >
          </div>
        </div>
      </div>
    </div>

    <div class="reveal" style="transition-delay: 150ms;">
      <div class="grid-card h-full">
        <img src={project_img_3} alt="ProjectImg" />
        <div class="flex flex-col gap-2 lg:gap-4">
          <h3>RealTime Chat</h3>
          <span
            >Implemented WebSocket-based messaging with a responsive interface.</span
          >
          <div class="tech-stack">
            <span>Node.js</span>
            <span>Express.js</span>
            <span>Socket.io</span>
            <span>Tailwind</span>
          </div>
          <div class="flex gap-2 lg:gap-5 w-fit m-auto">
            <a
              href="https://simple-chat-app-jmqz.onrender.com"
              target="_blank"
              aria-label="View live demo of realtime chat."
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 bg-linear-to-r from-[#4F8DFF] to-[#3B82F6] hover:-translate-y-1 active:scale-95"
                ><Livedemo class="w-4 h-4" />Live Demo</button
              ></a
            >

            <a
              href="https://github.com/divyansh-coder-git/simple-chat-app"
              target="_blank"
              aria-label="View source code of realtime chat on github."
            >
              <button
                class="flex gap-2 items-center rounded-2xl lg:rounded-[3rem] px-4 py-1 lg:py-2 lg:px-4 text-xs lg:text-base border border-[#4f8dff] cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 active:scale-95 hover:-translate-y-1"
                ><i class="fa-brands fa-github"></i>Github Repo</button
              ></a
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .grid-card {
    padding: 1.5rem 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    text-align: center;
    border: 1px solid var(--card-border-color);
    background-color: rgba(18, 36, 74, 0.75);
    backdrop-filter: blur(16px);
    /* border: 2x solid white */
    border-radius: 1.5rem;
    cursor: pointer;
    height: 100%;
    transition:
      transform 0.3s ease-in-out,
      box-shadow 0.3s ease-in-out,
      border-color 0.3s ease-in-out,
      background-color 0.3s ease-in-out;
  }

  .grid-card span {
    font-size: 0.9rem;
    color: #8892b0;
    transition: all 0.2s ease-in-out;
  }

  .grid-card:hover {
    border: 1px solid #4f8dff;
    background-color: var(--card-hober-bg-color);
    box-shadow: 0 0 20px rgba(79, 141, 255, 0.15);
    transform: translateY(-8px) scale(1.01);
  }

  .grid-card h3 {
    font-size: 1.5rem;
    font-weight: 500;
    transition: 0.2s ease-in-out;
  }

  .grid-card:hover h3 {
    color: #4f8dff;
    transform: scale(1.02);
  }

  .grid-card:hover span {
    color: var(--secondary-text-color);
    transform: translateY(-0.5rem);
  }

  .grid-card img {
    width: 20vw;
    border-radius: 1rem;
    margin-bottom: 2rem;
    border: 1px solid #0a3a4f;
    transition: all 0.2s ease-in-out;
  }

  .grid-card:hover img {
    transform: translateY(0.5rem) scale(1.02);
  }

  .tech-stack {
    display: flex;
    gap: 0.3rem;
    width: 100%;
    justify-content: center;
    transition: all 0.2s ease-in-out;
  }

  .tech-stack span {
    padding: 0 0.5rem;
    font-size: 0.85rem;
    background-color: var(--tag-bg-color);
    border: 1px solid var(--tag-border-color);
    border-radius: 0.25rem;
    color: var(--tag-text-color);
  }

  .grid-card:hover .tech-stack {
    transform: scale(1.02);
  }

  @media screen and (max-width: 1024px) {
    .grid-card {
      padding: 0.75rem 0.75rem;
      width: fit-content;
      border-radius: 1rem;
      margin: auto;
      border: 1px solid #0a3a4f;
    }

    .grid-card span {
      font-size: 0.7rem;
    }

    .grid-card h3 {
      font-size: 1.3rem;
    }

    .grid-card img {
      padding: 0.5rem 1rem;
      width: min-content;
      border-radius: 0.5rem;
      margin-bottom: 0.5rem;
      border: none;
    }

    .grid-card:hover img {
      transform: translateY(0.5rem) scale(1.07);
    }

    .grid-card:hover span {
      color: var(--secondary-text-color);
      transform: translateY(-0.5rem);
    }
  }
</style>
