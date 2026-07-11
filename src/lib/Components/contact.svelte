<script lang="ts">
  let name = $state("");
  let email = $state("");
  let message = $state("");
  let ph_number = $state("");

  let submitted = $state(false);
  let sending = $state(false);

  async function submitForm() {
    sending = true;

    const response = await fetch("https://formspree.io/f/xzdlbjpy", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
      body: JSON.stringify({
        name,
        email,
        ph_number,
        message,
      }),
    });

    if (response.ok) {
      submitted = true;

      // Clear fields
      name = "";
      email = "";
      ph_number = "";
      message = "";

      setTimeout(() => {
        submitted = false;
      }, 3000);
    }

    sending = false;
  }
</script>

<hr
  id="contact"
  class="w-[95vw] m-auto bg-[#0a3a4f] border-none h-px snap-start"
/>

<!-- <hr
  id="projects"
  class="w-[95vw] m-auto bg-[#0a3a4f] lg:bg-gray-200 border-none h-px snap-start"
/> -->
<div class="text-white min-h-screen flex flex-col lg:justify-end">
  <div
    class="flex flex-col justify-center lg:justify-around items-center gap-8 mb-10 flex-1"
  >
    <div class="m-0 p-0 h-14 w-full"></div>
    <h2 class="text-5xl lg:text-6xl text-[#ccd6f6] font-semibold text-center">
      Contact <span class="text-(--secondary-theme-text-color)">Me</span>
    </h2>
    <!-- mt-20 lg:mb-10 -->
    <form
      action="https://formspree.io/f/xzdlbjpy"
      method="post"
      onsubmit={(e) => {
        e.preventDefault();
        submitForm();
      }}
    >
      <div
        class="input-form flex flex-col lg:items-stretch items-center lg:flex-row lg:gap-10"
      >
        <div class="flex flex-col gap-2 lg:gap-3">
          <input
            bind:value={name}
            type="text"
            placeholder="Full Name"
            name="name"
            required
          />
          <input
            bind:value={email}
            type="email"
            placeholder="Email"
            name="email"
            required
          />
          <input
            bind:value={ph_number}
            type="tel"
            placeholder="Phone Number"
            name="phone_number"
          />
        </div>
        <div
          class="flex flex-col gap-1 mt-2 lg:mt-0 lg:gap-2 flex-1 items-center"
        >
          <textarea
            bind:value={message}
            class="px-4 py-1 w-[300px] text-[1.2rem] lg:text-base lg:px-3 lg:py-2 border-2 flex-1 border-black lg:w-xl h-full rounded-xl lg:rounded-2xl"
            placeholder="Message"
            name="message"
          ></textarea>
          <button
            type="submit"
            class="w-full bg-white text-black rounded-2xl lg:rounded-[3rem] text-[1.2rem] lg:text-base px-4 py-1 lg:py-2 lg:px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white"
            >{sending ? "Sending..." : "Submit"}</button
          >
          {#if submitted}
            <p class="text-green-400 lg:mt-4">
              <i class="fa-solid fa-check"></i> Message sent successfully
            </p>
          {/if}
        </div>
      </div>
    </form>
  </div>

  <div
    class="footer sticky bottom-0 left-0 flex flex-col justify-evenly items-center py-2 lg:py-3 text-white w-full border-t border-slate-500 bg-white/10 backdrop-blur"
  >
    <div class="socials flex gap-3 lg:gap-3 lg:py-1">
      <a
        href="https://github.com/divyansh-coder-git"
        target="_blank"
        aria-label="SocialLinks"><i class="fa-brands fa-github"></i></a
      >
      <a
        href="https://www.linkedin.com/in/divyansh-pandey-nits/"
        target="_blank"
        aria-label="SocialLinks"><i class="fa-brands fa-linkedin"></i></a
      >

      <a
        href="https://instagram.com/divyansh_coder"
        target="_blank"
        aria-label="SocialLinks"><i class="fa-brands fa-instagram"></i></a
      >
    </div>

    <div class="links">
      <ul class="flex text-sm gap-2">
        <li>
          <a href="#projects">Projects</a>
        </li>
        <li>
          <a href="#about">About</a>
        </li>
        <li>
          <a href="#experience">Skills</a>
        </li>
        <li>
          <a href="#contact">Contacts</a>
        </li>
      </ul>
    </div>

    <div class="copyright py-2">
      <p class="text-sm text-[#8892b0] font-light">
        © Divyansh Pandey | All Rights Reserved
      </p>
    </div>

    <div class="credits">
      <p class="text-xs text-[#8892b0] font-light text-center">
        Credits: isometric PNG Designed By from <a
          href="https://pngtree.com/freepng/web-developer-isometric-illustration_6067558.html?sol=downref&id=bef"
          target="_blank"
          >https://pngtree.com/freepng/web-developer-isometric-illustration_6067558.html?sol=downref&id=bef</a
        >
        internet clipart PNG Designed By from
        <a
          href="https://pngtree.com/freepng/web-development-illustration-modern_4461019.html?sol=downref&id=bef"
          target="_blank"
          >https://pngtree.com/freepng/web-development-illustration-modern_4461019.html?sol=downref&id=bef</a
        >
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

  .input-form textarea {
    background-color: rgb(42, 46, 50);
  }

  .socials i {
    font-size: 1.5rem;
    cursor: pointer;
    transition: 0.3s ease-in-out;
  }

  .socials i:hover {
    transform: scale(1.1);
    color: #38bdf8;
  }

  .links a {
    position: relative;
    color: white;
    font-weight: 300;
    font-size: 0.875rem;
  }

  .links a:hover {
    color: #38bdf8;
  }

  .links a::before {
    position: absolute;
    content: "";
    width: 0px;
    left: 0px;
    height: 3px;
    top: 20px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: #38bdf8;
  }

  .links a:hover::before {
    width: 100%;
  }

  @media screen and (max-width: 1024px) {
    .input-form input {
      font-size: 1.2rem;
      height: 3rem;
      width: 300px;
      padding: 1rem 1rem;
      border: 2px solid black;
      border-radius: 0.5rem;
      background-color: rgb(42, 46, 50);
    }

    .socials i {
      font-size: 1.5rem;
      cursor: pointer;
      transition: 0.3s ease-in-out;
    }

    .links a {
      position: relative;
      color: white;
      font-weight: 300;
      font-size: 0.8rem;
    }
    .links a::before {
      position: absolute;
      content: "";
      width: 0px;
      left: 0px;
      height: 3px;
      top: 17px;
      border-radius: 1rem;
      transition: 0.3s ease-in-out;
      background: #38bdf8;
    }

    .links a:hover::before {
      width: 100%;
    }
  }
</style>
