<script lang="ts">
  import cover_img from "$lib/assets/github-3.png";
</script>
<hr id="experience" class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start">
<div class="h-[85vh] flex flex-col scroll-smooth snap-center mt-25 px-10">
  <h1 class="text-7xl font-semibold text-center mb-12">Experience</h1>
  <div class="flex items-center justify-center gap-10">
    <div class="grid grid-cols-2 gap-8 px-10">
      <div class="grid-card">
        <i class="fa-solid fa-code"></i>
        <h1>Frontent Development</h1>
        <h3>2 years</h3>
        <span
          >Lorem ipsum dolor sit amet consectetur adipisicing elit.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-file-code"></i>
        <h1>Backend Development</h1>
        <h3>1 years</h3>
        <span
          >Lorem ipsum dolor sit amet consectetur adipisicing elit.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-brands fa-python"></i>
        <h1>Python Development</h1>
        <h3>4 years</h3>
        <span
          >Lorem ipsum dolor sit amet consectetur adipisicing elit.</span
        >
      </div>

      <div class="grid-card">
        <i class="fa-solid fa-brain"></i>
        <h1>Machine Learning</h1>
        <h3>3 years</h3>
        <span
          >Lorem ipsum dolor sit amet consectetur adipisicing elit.</span
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
    border: 2px solid black;
    border-radius: 3rem;
    align-items: baseline;
    justify-content: left;
    cursor: pointer;
    transition: 0.5s ease-in-out;
  }

  .grid-card:hover {
    transform: scale(1.05);
    background-color: black;
    color: white;
  }

  .grid-card i{
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .grid-card h1{
    font-size: 1.5rem;
    font-weight: 500;
  }

  .grid-card h3{
    font-weight: 500;
  }
</style>
