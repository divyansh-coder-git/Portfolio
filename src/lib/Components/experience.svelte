<script lang="ts">
  import cover_img from "$lib/assets/img2.png";
</script>

<hr
  id="experience"
  class="w-[95vw] m-auto bg-[#0a3a4f] border-none h-px snap-start"
/>

<!-- <hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] md:bg-gray-200 border-none h-px snap-start"
/> -->
<div
  class="text-white h-screen md:h-screen flex flex-col scroll-smooth md:justify-around snap-center md:px-10"
>
<!-- mt-5 md:mt-20 -->
<div class="m-0 p-0 h-12 w-full"></div>
  <h1
    class="text-4xl md:text-7xl text-[#ccd6f6] font-semibold text-center mb-5 md:mb-0"
  >
    Skills & Interests
  </h1>
   <!-- mb-6 md:mb-5 -->
  <div
    class="flex flex-col md:flex-row items-center justify-center md:gap-10 flex-1 md:flex-none"
  >
    <div
      class="flex flex-col justify-around md:grid md:grid-cols-2 gap-4 md:gap-6 px-10 flex-1 pb-5 md:pb-0"
    >
      <div class="grid-card">
        <i class="fa-solid fa-code"></i>
        <h1>Web Development</h1>
        <span
          >Building responsive web applications using Svelte, TypeScript and
          Tailwind CSS. Focused on creating clean user interfaces and learning
          modern frontend development.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-file-code"></i>
        <h1>Machine Learning</h1>
        <span
          >Currently learning Machine Learning through Andrew Ng's course and
          Summer Analytics 2026, exploring supervised learning and model
          building.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-brands fa-python"></i>
        <h1>Python Development</h1>
        <span
          >Using Python for problem solving, automation and machine learning
          projects. Familiar with NumPy, data handling and object-oriented
          programming.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-brain"></i>
        <h1>Problem Solving</h1>
        <span
          >Strengthening analytical thinking through engineering coursework,
          programming and project development.</span
        >
      </div>
    </div>
    <img
      class="hidden md:block md:w-[25vw] md:h-auto md:object-cover"
      src={cover_img}
      alt="CoverImage"
    />
  </div>
</div>

<style>
  .grid-card {
    padding: 1.5rem 2rem;
    display: flex;
    flex-direction: column;
    border: 2px solid #0a3a4f;
    /* border: 2px solid white */
    border-radius: 3rem;
    align-items: baseline;
    justify-content: left;
    cursor: pointer;
    transition: 0.5s ease-in-out;
  }

  .grid-card span {
    font-size: 0.9rem;
    color: #8892b0;
  }

  .grid-card:hover {
    transform: scale(1.05);
    background-color: white;
    color: black;
  }

  .grid-card:hover span {
    color: black;
  }

  .grid-card i {
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .grid-card h1 {
    font-size: 1.5rem;
    font-weight: 500;
  }

  @media screen and (max-width: 768px) {
    .grid-card {
      padding: 1rem 1rem;
      border-radius: 1rem;
      border: 1px solid #0a3a4f;
    }

    .grid-card span {
      font-size: 0.7rem;
    }

    .grid-card i {
      font-size: 1rem;
      margin-bottom: 0rem;
    }

    .grid-card h1 {
      font-size: 1rem;
    }
  }
</style>
