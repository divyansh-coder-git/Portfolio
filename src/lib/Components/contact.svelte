<script lang="ts">
  import Send from "@lucide/svelte/icons/send-horizontal";
  import Mail from "@lucide/svelte/icons/mail";
  import Pin from "@lucide/svelte/icons/map-pin";
  import Clock from "@lucide/svelte/icons/clock-3";

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

  import { onMount } from "svelte";

  onMount(() => {
    const cards = document.querySelectorAll(".reveal");

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("show");
            observer.unobserve(entry.target);
          }
        });
      },
      {
        threshold: 0.2,
      },
    );

    cards.forEach((card) => observer.observe(card));
  });
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
  <div class="flex flex-col justify-center items-center gap-8 mb-10 flex-1">
    <div class="m-0 p-0 h-14 w-full"></div>

    <div class="reveal">
      <h2 class="text-5xl lg:text-6xl text-[#ccd6f6] font-semibold text-center">
        Contact <span class="text-(--secondary-theme-text-color)">Me</span>
        <span class="block text-base font-light px-5 lg:px-0"
          >Have an idea, internship opportunity, or just want to say hi? Feel
          free to reach out.</span
        >
      </h2>
    </div>

    <div
      class="flex flex-col-reverse lg:flex-row gap-5 lg:gap-10 items-center justify-center"
    >
      <div class="reveal" style="transition-delay: 500ms;">
        <div
          class="info-pane flex flex-col gap-4 bg-(--card-bg-color) border rounded-xl border-(--card-border-color) px-7 py-3 hover:border-(--card-hover-border-color) transition-colors duration-150"
        >
          <h1
            class="w-full flex flex-col items-center text-xl lg:text-2xl text-(--primary-text-color)"
          >
            Get in touch
            <div
              class="w-37.5 h-0.5 rounded-full mt-2 bg-linear-to-r from-[#4F8DFF] to-[#-[#6FA9FF]"
            ></div>
          </h1>

          <div class="email">
            <span
              class="flex gap-1 lg:gap-2 items-center text-(--secondary-text-color) text-sm lg:text-base"
              ><Mail class="w-4 h-4 lg:w-5 lg:h-5 text-[#6FA9FF]" />Email</span
            >
            <span class="text-sm lg:text-base text-(--description-text-color)"
              >divyanshpandey062@gmail.com</span
            >
          </div>

          <div class="location">
            <span
              class="flex gap-1 lg:gap-2 items-center text-(--secondary-text-color) text-sm lg:text-base"
              ><Pin
                class="w-4 h-4 lg:w-5 lg:h-5 text-[#6FA9FF]"
              />Location</span
            >
            <span class="text-sm lg:text-base text-(--description-text-color)"
              >NIT Silchar, Assam, India</span
            >
          </div>

          <div class="time">
            <span
              class="flex gap-1 lg:gap-2 items-center text-(--secondary-text-color) text-sm lg:text-base"
              ><Clock class="w-4 h-4 lg:w-5 lg:h-5 text-[#6FA9FF]" />Response
              Time</span
            >
            <span class="text-sm lg:text-base text-(--description-text-color)"
              >Usually within 24 hours</span
            >
          </div>

          <div
            class="social-info hidden lg:flex w-full justify-center items-center gap-3 lg:gap-5"
          >
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
              href="https://instagram.com/divyansh._.pandey__/"
              target="_blank"
              aria-label="SocialLinks"><i class="fa-brands fa-instagram"></i></a
            >
          </div>
        </div>
      </div>
      <!-- mt-20 lg:mb-10 -->

      <div class="reveal">
        <form
          action="https://formspree.io/f/xzdlbjpy"
          method="post"
          onsubmit={(e) => {
            e.preventDefault();
            submitForm();
          }}
        >
          <div
            class="input-form flex flex-col lg:items-stretch items-center lg:flex-row lg:gap-6 lg:border lg:rounded-xl lg:px-5 lg:py-5.5 lg:border-(--card-border-color) lg:bg-(--card-bg-color)"
          >
            <div class="flex flex-col gap-1 lg:gap-3">
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
            <div class="flex flex-col gap-2 mt-1 lg:mt-0 flex-1 items-center">
              <textarea
                bind:value={message}
                class="message-text px-4 py-1 w-[300px] text-[1rem] lg:text-lg lg:px-3 lg:py-2 border-2 flex-1 lg:w-xl h-full rounded-xl lg:rounded-2xl"
                placeholder="Message"
                name="message"
              ></textarea>
              <button
                type="submit"
                class="overflow-hidden group flex gap-3 items-center justify-center w-full bg-linear-to-r from-[#4F8DFF] to-[#3B82F6] text-white rounded-2xl lg:rounded-[3rem] text-[1rem] lg:text-lg px-4 py-1 lg:py-2 lg:px-6 cursor-pointer font-medium text-nowrap transition-all ease-in-out duration-200 hover:translate-y-0.5 active:scale-95 lg:h-11.25"
                >{sending ? "Sending..." : "Submit"}<Send
                  class="w-5 h-5 font-bold transition-all group-hover:scale-x-110 group-hover:translate-x-2"
                /></button
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
    </div>
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
        href="https://instagram.com/divyansh._.pandey__/"
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
    height: 4rem;
    padding: 0.5rem 0.75rem;
    border: 1px solid #22476e;
    border-radius: 1rem;
    /* background-color: rgb(42, 46, 50);*/
    background: -color rgba(18, 36, 74, 0.75);
    color: #f6f9ff;
  }

  .input-form input::placeholder {
    color: #8d9cb8;
  }

  .input-form button:hover {
    box-shadow: 0 5px 20px rgba(79, 141, 255, 0.3);
  }

  .input-form input:focus {
    outline: none;
    border-color: #4f8dff;
    box-shadow: 0 0 18px var(--box-shadow-color);
  }

  .input-form textarea {
    border: 1px solid #22476e;
    background-color: rgba(18, 36, 74, 0.75);
    color: #f6f9ff;
  }

  .input-form textarea::placeholder {
    color: #8d9cb8;
  }

  .input-form textarea:focus {
    outline: none;
    border-color: #4f8dff;
    box-shadow: 0 0 18px var(--box-shadow-color);
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

  .social-info i {
    font-size: 2rem;
    cursor: pointer;
    transition: 0.3s ease-in-out;
    border-radius: 100%;
    color: var(--secondary-text-color);
  }

  .social-info i:hover {
    transform: translateY(-3px) scale(1.02);
    color: var(--secondary-theme-text-color);
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

  .info-pane:hover {
    box-shadow: 0 0 20px rgba(79, 141, 255, 0.12);
  }

  @media screen and (max-width: 1024px) {
    .input-form input {
      font-size: 1rem;
      height: 2.3rem;
      width: 300px;
      padding: 1rem 0.5rem;
      border-radius: 0.5rem;
    }

    .message-text {
      border-radius: 0.5rem;
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
