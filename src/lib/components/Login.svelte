<script>
  import { userName } from "$lib/store";
  let date = new Date();
  $: hour = String(date.getHours()).padStart(2, "0");
  $: minutes = String(date.getMinutes()).padStart(2, "0");
</script>

<div class="relative flex items-center justify-center h-screen w-screen">
  <div
    class="absolute inline-flex flex-col align-center justify-center w-1/2 h-[55%] z-20 p-10 text-white text-center gap-y-[10%]"
  >
    <h1 class="text-3xl font-bold">Welcome to Svelte Linux</h1>
    <div class="text-8xl font-extrabold">
      {hour} : {minutes}
    </div>
    <div class="font-bold z-20">
      <label class="text-3xl"
        >USERNAME :
        <input
          type="text"
          bind:value={$userName}
          autocorrect="off"
          class="text-center p-2 rounded-[1.5rem] border-white border-4 bg-transparent"
        />
      </label>
    </div>
    <div>
      <a
        type="button"
        class="font-bold w-1/3 rounded-full border-white border-4 text-3xl"
        href="/desktop">LOGIN</a
      >
    </div>
  </div>
  <svg
    viewBox="0 0 960 590"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    class="h-[55%] w-1/2 stroke-white stroke-width-[5] z-10"
    preserveAspectRatio="none"
  >
    <rect
      x="2.5"
      y="2.5"
      width="955"
      height="585"
      rx="27.5"
      stroke="white"
      stroke-width="5"
    />
  </svg>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    class="object-cover object-center h-screen w-screen absolute top-0 left-0 mix-blend-color backdrop-blur-[12.5px]"
    viewBox="0 0 1920 1080"
    fill="none"
    preserveAspectRatio="none"
  >
    <g class="mix-blend-color" filter="url(#filter0_b_128_8)">
      <path
        class="fill-black"
        fill-rule="evenodd"
        clip-rule="evenodd"
        d="M1920 0H0V1080H1920V0ZM510 245C493.431 245 480 258.431 480 275V805C480 821.569 493.431 835 510 835H1410C1426.57 835 1440 821.569 1440 805V275C1440 258.431 1426.57 245 1410 245H510Z"
      />
    </g>
    <defs>
      <filter
        id="filter0_b_128_8"
        x="-25"
        y="-25"
        width="1970"
        height="1130"
        filterUnits="userSpaceOnUse"
        color-interpolation-filters="sRGB"
      >
        <feFlood flood-opacity="0" result="BackgroundImageFix" />
        <feGaussianBlur in="BackgroundImageFix" stdDeviation="12.5" />
        <feComposite
          in2="SourceAlpha"
          operator="in"
          result="effect1_backgroundBlur_128_8"
        />
        <feBlend
          mode="normal"
          in="SourceGraphic"
          in2="effect1_backgroundBlur_128_8"
          result="shape"
        />
      </filter>
    </defs>
  </svg>
</div>
