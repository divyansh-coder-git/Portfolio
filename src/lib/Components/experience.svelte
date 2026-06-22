<script lang="ts">
  import cover_img from "$lib/assets/github-3.png";
</script>
<hr id="experience" class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start">
<div class="text-white h-[90vh] flex flex-col scroll-smooth snap-center mt-25 px-10">
  <h1 class="text-7xl font-semibold text-center mb-12">Skills & Interests</h1>
  <div class="flex items-center justify-center gap-10">
    <div class="grid grid-cols-2 gap-6 px-10">
      <div class="grid-card">
        <i class="fa-solid fa-code"></i>
        <h1>Web Development</h1>
        <span
          >Building responsive web applications using Svelte, TypeScript and Tailwind CSS. Focused on creating clean user interfaces and learning modern frontend development.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-file-code"></i>
        <h1>Machine Learning</h1>
        <span
          >Currently learning Machine Learning through Andrew Ng's course and Summer Analytics 2026, exploring supervised learning and model building.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-brands fa-python"></i>
        <h1>Python Development</h1>
        <span
          >Using Python for problem solving, automation and machine learning projects. Familiar with NumPy, data handling and object-oriented programming.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-brain"></i>
        <h1>Problem Solving</h1>
        <span
          >Strengthening analytical thinking through engineering coursework, programming and project development.</span
        >
      </div>
    </div>
    <img class="w-[25vw] h-auto object-cover" src={cover_img} alt="CoverImage" />
  </div>
</div>

<style>
  .grid-card {
    padding: 1.5rem 2rem;
    display: flex;
    flex-direction: column;
    border: 2px solid white;
    border-radius: 3rem;
    align-items: baseline;
    justify-content: left;
    cursor: pointer;
    transition: 0.5s ease-in-out;
  }

  .grid-card:hover {
    transform: scale(1.05);
    background-color: white;
    color: black;
  }

  .grid-card i{
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .grid-card h1{
    font-size: 1.5rem;
    font-weight: 500;
  }

  .grid-card span{
    font-size: 0.90rem;
  }
</style>
