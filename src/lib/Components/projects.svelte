<script lang="ts">
  import project_img from "$lib/assets/project1.png";
</script>

<hr id="projects" class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start" />

<div class="min-h-screen flex flex-col scroll-smooth snap-center mt-25 px-15">
  <h1 class="text-7xl font-semibold text-center mb-12">Recent Projects</h1>

  <div class="grid grid-cols-3 gap-8 px-10">
    <div class="grid-card">
      <img src={project_img} alt="ProjectImg" />
      <div class="flex flex-col gap-4">
        <h3>Habit Tracker</h3>
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit.</span>
        <div class="flex gap-5">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Live Demo</button
          >
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Github Repo</button
          >
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img} alt="ProjectImg" />
      <div class="flex flex-col gap-4">
        <h3>Project 2</h3>
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit.</span>
        <div class="flex gap-5">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Live Demo</button
          >
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Github Repo</button
          >
        </div>
      </div>
    </div>

    <div class="grid-card">
      <img src={project_img} alt="ProjectImg" />
      <div class="flex flex-col gap-4">

        <h3>Project 1</h3>
        <span>Lorem ipsum dolor sit amet consectetur adipisicing elit.</span>

        <div class="flex gap-5">
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Live Demo</button
          >
          <button
            class="rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >Github Repo</button
          >
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
    justify-content: center;
    text-align: center;
    border: 2px solid black;
    border-radius: 3rem;
    cursor: pointer;
    transition: 0.3s ease-in-out;
  }

  .grid-card:hover {
    transform: translateY(-10px)scale(1.02);
    background-color: black;
    color: white;
  }

  .grid-card:hover button{
    border: 2px solid white;
    color: white;
  }

  .grid-card:hover button:hover{
    border: 2px solid white;
    background: white;
    color: black;
  }

  .grid-card img {
    width: 20vw;
    border-radius: 1rem;
  }

  .grid-card h3{
    font-size: 2rem;
    font-weight: 500;
  }
</style>
