<script>
  import Step from "./Step.svelte";

  let steps = [
    {
      name: "On Tyranny selector",
      icon: "fa-solid fa-book",
    },
    {
      name: "Snake game",
      icon: "fa-solid fa-gamepad",
    },
    {
      name: "Pong game",
      icon: "fa-solid fa-table-tennis-paddle-ball",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I am <span class="poppins text-violet-400">Damian</span> Drábek
        <br />
        Full Stack <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favourite tech</span> includes JavaScript
        (SvelteKit or React), TailwindCSS, Node.js + Express.js & PostgreSQL or Firebase/Firestore!
      </p>
      <a
        href="https://instagram.com/damian.drabek"
        target="_blank"
        class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="realtive shadow-2xl grid place-items-center">
      <img
        src={"images/profile.png"}
        alt="Profile image"
        class="object-cover z-[2] max-h-[70vh] rounded-full"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center md:text-2xl">
      <h6 class="text-lg sm:text-xl">A few of my creative endeavors.</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href="https://youtube.com/@damiandrabek"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play"></i>
      <p>Watch the video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          This selector chooses a random chapter Timothy Snyder's book <strong
            class="text-violet-400">On Tyranny</strong
          >. If you don't want it select the same chapter again, just put it to
          the read ones.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          Let's you play the OG <strong class="text-violet-400">Snake</strong>.
          Bet you can't outscore me!
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          Play your old favourite game of <strong class="text-violet-400"
            >Pong</strong
          > against a bots of various difficulties. You haven't a seen a real opponent
          until the hardest bot.
        </p>
      </Step>
    </div>
  </section>

  <section id="about"></section>
</main>
