<script lang="ts">
  import project_img_1 from "$lib/assets/project1.png";
  import project_img_2 from "$lib/assets/project2.png";
  import project_img_3 from "$lib/assets/project4.png";
</script>

<hr
  id="projects"
  class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start"
/>

<div
  class="text-white min-h-screen flex flex-col scroll-smooth snap-center mt-25 px-15"
>
  <h1 class="text-7xl text-[#ccd6f6] font-semibold text-center mb-12">
    Recent Projects
  </h1>

  <div class="grid grid-cols-3 gap-8 px-10">
    <div class="grid-card">
      <img src={project_img_1} alt="ProjectImg" />
      <div class="flex flex-col gap-4">
        <h3>Habit Tracker</h3>
        <span>Track daily habits, monitor streaks and stay consistent.</span>

        <span class="font-semibold">Svelte • TS • Tailwind</span>
        <div class="flex gap-5 w-fit m-auto">
          <a href="https://habit-tracker-svelte.netlify.app/" target="_blank">
            <button
              class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
              >Live Demo</button
            ></a
          >
          <a
            href="https://github.com/divyansh-coder-git/habit-tracker-svelte"
            target="_blank"
          >
            <button
              class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
              >Github Repo</button
            ></a
          >
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img_2} alt="ProjectImg" />
      <div class="flex flex-col gap-4">
        <h3>Portfolio Website</h3>
        <span>Personal portfolio showcasing projects, skills and experience.</span>
        <span class="font-semibold">Svelte • TS • Tailwind</span>
        <div class="flex gap-5 w-fit m-auto">
        <a href="https://divyansh-pandey.netlify.app/" target="_blank">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Live Demo</button
          ></a>
          <a href="https://github.com/divyansh-coder-git/Portfolio" target="_blank">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Github Repo</button
          ></a>
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img_3} alt="ProjectImg" />

      <div class="flex flex-col gap-4">
        <h3>Summer Analytics 2026</h3>
        <span>Machine learning coursework and practical assignments.</span>
        <span class="font-semibold">Python • NumPy • ML</span>
        <div class="flex gap-5 w-fit m-auto">
        <a href="https://www.hackerearth.com/community/challenges/hackathon/summer-analytics-2026/" target="_blank">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
            >Live Demo</button
          ></a>

          <a href="https://github.com/divyansh-coder-git" target="_blank">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-white cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300"
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
    border: 1px solid white;
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
</style>
