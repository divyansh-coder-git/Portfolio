<script lang="ts">
</script>

<div
  class="footer flex flex-col justify-evenly items-center py-5 text-white w-full left-0 bottom-0 bg-black/80 backdrop-blur"
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
    <p class="text-sm text-gray-200">
      © Divyansh Pandey | All Rights Reserved
    </p>
  </div>
</div>

<style>
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
    color: white;
    font-weight: 300;
    font-size: 1.2rem;
  }

  .links a::before{
    position: absolute;
    content: "";
    width: 0px;
    left: 0px;
    height: 3px;
    top: 25px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: white;
  }

  .links a:hover::before{
    width: 100%;
  }
</style>
