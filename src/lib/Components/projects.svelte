<script lang="ts">
  import project_img_1 from "$lib/assets/project1.png";
  import project_img_2 from "$lib/assets/project2.png";
  import project_img_3 from "$lib/assets/project5.png";
</script>

<hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] border-none h-px snap-start"
/>



<!-- <hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] md:bg-gray-200 border-none h-px snap-start"
/> -->

<div
  class="text-white min-h-screen flex flex-col scroll-smooth snap-center md:justify-around px-10 md:px-15"
>
<!-- md:mt-25 -->
 <!-- mt-5 -->
<div class="m-0 p-0 h-12 w-full"></div>
  <h1 class="text-4xl md:text-7xl text-[#ccd6f6] font-semibold text-center md:mb-3">
    Recent Projects
  </h1>
  <!-- md:mb-12 -->

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-8 px-5 py-7 md:px-10 md:py-0">
    <div class="grid-card">
      <img src={project_img_1} alt="ProjectImg" />
      <div class="flex flex-col gap-2 md:gap-4">
        <h3>Habit Tracker</h3>
        <span>Track daily habits, monitor streaks and stay consistent.</span>

        <span class="font-semibold">Svelte • TS • Tailwind</span>
        <div class="flex gap-2 md:gap-5 w-fit m-auto">
          <a href="https://habit-tracker-svelte.netlify.app/" target="_blank">
            <button
              class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
              >Live Demo</button
            ></a
          >
          <a
            href="https://github.com/divyansh-coder-git/habit-tracker-svelte"
            target="_blank"
          >
            <button
              class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
              >Github Repo</button
            ></a
          >
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img_2} alt="ProjectImg" />
      <div class="flex flex-col gap-2 md:gap-4">
        <h3>Portfolio Website</h3>
        <span>Personal portfolio showcasing projects, skills and experience.</span>
        <span class="font-semibold">Svelte • TS • Tailwind</span>
        <div class="flex gap-2 md:gap-5 w-fit m-auto">
        <a href="https://divyansh-pandey.netlify.app/" target="_blank">
          <button
            class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Live Demo</button
          ></a>
          <a href="https://github.com/divyansh-coder-git/Portfolio" target="_blank">
          <button
            class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Github Repo</button
          ></a>
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img_3} alt="ProjectImg" />

      <div class="flex flex-col gap-2 md:gap-4">
        <h3>SyncChat</h3>
        <span>Real-time chat application built using Node.js, Express, and Socket.io.</span>
        <span class="font-semibold">Node.js • Express.js • Socket.io • CSS</span>
        <div class="flex gap-2 md:gap-5 w-fit m-auto">
        <a href="https://simple-chat-app-jmqz.onrender.com" target="_blank">
          <button
            class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Live Demo</button
          ></a>

          <a href="https://github.com/divyansh-coder-git/simple-chat-app" target="_blank">
          <button
            class="rounded-2xl md:rounded-[3rem] px-4 py-1 md:py-2 md:px-6 text-sm md:text-base border md:border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Github Repo</button
          ></a>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .grid-card {
    padding: 2rem 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    text-align: center;
    border: 1px solid #0a3a4f;
    /* border: 2x solid white */
    border-radius: 3rem;
    cursor: pointer;
    transition: 0.3s ease-in-out;
  }

  .grid-card span {
    font-size: 0.9rem;
    color: #8892b0;
  }

  .grid-card:hover {
    transform: translateY(-10px) scale(1.02);
    background-color: white;
    backdrop-filter: blur(8px);
    border-color: #60a5fa;
    color: black;
  }

  .grid-card:hover button {
    border: 2px solid black;
    color: black;
  }

  .grid-card:hover button:hover {
    border: 2px solid black;
    background: black;
    color: white;
  }

  .grid-card img {
    width: 20vw;
    border-radius: 1rem;
    margin-bottom: 2rem;
    border: 1px solid #0a3a4f;
  }

  .grid-card h3 {
    font-size: 1.5rem;
    font-weight: 500;
  }

  @media screen and (max-width: 640px) {
  .grid-card{
    padding: 0.75rem 0.75rem;
    border-radius: 1rem;
    border: 1px solid #0a3a4f;
  }

  .grid-card span{
    font-size: 0.7rem;
  }

  .grid-card h3{
    font-size: 1.3rem;
  }

  .grid-card img {
    padding: 0.5rem 1rem;
    width:min-content;
    border-radius: 0.25rem;
    margin-bottom: 0.5rem;
    border: none;
  }
}
</style>
