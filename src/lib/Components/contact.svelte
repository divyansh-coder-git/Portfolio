<script lang="ts">
</script>

<hr id="contact" class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start" />
<div class="text-white min-h-screen flex flex-col justify-end">
  <div class="flex flex-col justify-center items-center gap-8 mb-15">
  <h2 class="text-7xl font-semibold text-center mb-10">Contact Me</h2>
  <form>
    <div class="input-form flex gap-10">
      <div class="flex flex-col gap-3">
        <input type="text" placeholder="Full Name" />
        <input type="email" placeholder="Email" />
        <input type="number" placeholder="Phone Number" />
      </div>
      <div class="flex flex-col gap-2 items-center">
        <textarea
          class="px-3 py-2 border-2 border-black w-xl h-full rounded-2xl"
          placeholder="Message"></textarea>
        <button
          type="button"
          class="bg-white text-black rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white w-full"
          >Submit</button
        >
      </div>
    </div>
  </form>
  </div>

  <div
    class="footer sticky flex flex-col justify-evenly items-center py-5 text-black w-full left-0 bottom-0 border-t border-slate-500 bg-white/10 backdrop-blur"
  >
    <div class="socials flex gap-3 py-2">
      <a href="https://github.com" aria-label="SocialLinks"
        ><i class="fa-brands fa-github"></i></a
      >
      <a href="https://linkeddin.com" aria-label="SocialLinks"
        ><i class="fa-brands fa-linkedin"></i></a
      >
      <a href="https://instagram.com" aria-label="SocialLinks"
        ><i class="fa-brands fa-instagram"></i></a
      >
    </div>

    <div class="links py-2">
      <ul class="flex gap-3">
        <li>
          <a href="#faqs">FAQs</a>
        </li>
        <li>
          <a href="#services">Services</a>
        </li>
        <li>
          <a href="#about">About</a>
        </li>
        <li>
          <a href="#experience">Experience</a>
        </li>
      </ul>
    </div>

    <div class="copyright py-2">
      <p class="text-sm text-black">
        © Divyansh Pandey | All Rights Reserved
      </p>
    </div>
  </div>
</div>

<style>
  .input-form input {
    font-size: 1.3rem;
    height: 3.5rem;
    padding: 0.5rem 0.75rem;
    border: 2px solid black;
    border-radius: 1rem;
    background-color: rgb(42, 46, 50);
  }

  .input-form textarea{
    background-color: rgb(42, 46, 50);
  }

  .socials i {
    font-size: 2.5rem;
    cursor: pointer;
    transition: 0.3s ease-in-out;
  }

  .socials i:hover {
    transform: scale(1.1);
  }

  .links a {
    position: relative;
    color: black;
    font-weight: 300;
    font-size: 1.2rem;
  }

  .links a::before {
    position: absolute;
    content: "";
    width: 0px;
    left: 0px;
    height: 3px;
    top: 25px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: black;
  }

  .links a:hover::before {
    width: 100%;
  }
</style>
