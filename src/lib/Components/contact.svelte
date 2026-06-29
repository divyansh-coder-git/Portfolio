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
  class="w-[95vw] m-auto bg-gray-200 border-none h-px snap-start"
/>
<div class="text-white min-h-screen flex flex-col justify-end">
  <div class="flex flex-col justify-center items-center gap-8 mb-10">
    <h2 class="text-7xl text-[#ccd6f6] font-semibold text-center mb-10">
      Contact Me
    </h2>
    <form
      action="https://formspree.io/f/xzdlbjpy"
      method="post"
      onsubmit={(e) => {
        e.preventDefault();
        submitForm();
      }}
    >
      <div class="input-form flex gap-10">
        <div class="flex flex-col gap-3">
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
        <div class="flex flex-col gap-2 items-center">
          <textarea
            bind:value={message}
            class="px-3 py-2 border-2 border-black w-xl h-full rounded-2xl"
            placeholder="Message"
            name="message"
          ></textarea>
          <button
            type="submit"
            class="bg-white text-black rounded-[3rem] py-2 px-6 border-2 border-black cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-300 hover:bg-black hover:text-white w-full"
            >{sending ? "Sending..." : "Submit"}</button
          >
          {#if submitted}
            <p class="text-green-400 mt-4">
              <i class="fa-solid fa-check"></i> Message sent successfully
            </p>
          {/if}
        </div>
      </div>
    </form>
  </div>

  <div
    class="footer sticky flex flex-col justify-evenly items-center py-5 text-white w-full left-0 bottom-0 border-t border-slate-500 bg-white/10 backdrop-blur"
  >
    <div class="socials flex gap-3 py-2">
      <a href="https://github.com/divyansh-coder-git" target="_blank" aria-label="SocialLinks"
        ><i class="fa-brands fa-github"></i></a
      >
      <a href="https://www.linkedin.com/in/divyansh-pandey-nits/" target="_blank" aria-label="SocialLinks"
        ><i class="fa-brands fa-linkedin"></i></a
      >
      <a href="https://instagram.com/divyansh_coder" target="_blank" aria-label="SocialLinks"
        ><i class="fa-brands fa-instagram"></i></a
      >
    </div>

    <div class="links py-2">
      <ul class="flex gap-3">
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
          <a href="#contacts">Contacts</a>
        </li>
      </ul>
    </div>

    <div class="copyright py-2">
      <p class="text-sm text-[#8892b0] font-light">
        © Divyansh Pandey | All Rights Reserved
      </p>
    </div>

    <div class="credits">
      <p class="text-sm text-[#8892b0] font-light text-center">
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
    font-size: 2.5rem;
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
    font-size: 1.2rem;
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
    top: 25px;
    border-radius: 1rem;
    transition: 0.3s ease-in-out;
    background: #38bdf8;
  }

  .links a:hover::before {
    width: 100%;
  }
</style>
