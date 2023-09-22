<script>
  import { userName } from "$lib/store";
  let date = new Date();
  $: hour = String(date.getHours()).padStart(2, "0");
  $: minutes = String(date.getMinutes()).padStart(2, "0");
  $: month = String(date.toLocaleString("default", { month: "long" }));
  $: day = String(date.getDay());
  $: year = String(date.getFullYear());
</script>

<div class="p-[1%]">
  <div
    class="text-white rounded-full bg-white/50 flex flex-row justify-between w-full h-auto gap-x-2"
  >
    <div class="w-1/5 flex flex-row gap-x-4 align-center justify-left">
      <div
        class="bg-black/50 border-white border-2 rounded-l-full h-auto w-10 inline-flex flex-col align-center justify-center"
      >
        <a
          class="w-full inline-flex flex-col align-center justify-center"
          href="/"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="rotate-180 h-3/4 fill-white"
            viewBox="0 0 512 512"
            ><path
              d="M377.9 105.9L500.7 228.7c7.2 7.2 11.3 17.1 11.3 27.3s-4.1 20.1-11.3 27.3L377.9 406.1c-6.4 6.4-15 9.9-24 9.9c-18.7 0-33.9-15.2-33.9-33.9l0-62.1-128 0c-17.7 0-32-14.3-32-32l0-64c0-17.7 14.3-32 32-32l128 0 0-62.1c0-18.7 15.2-33.9 33.9-33.9c9 0 17.6 3.6 24 9.9zM160 96L96 96c-17.7 0-32 14.3-32 32l0 256c0 17.7 14.3 32 32 32l64 0c17.7 0 32 14.3 32 32s-14.3 32-32 32l-64 0c-53 0-96-43-96-96L0 128C0 75 43 32 96 32l64 0c17.7 0 32 14.3 32 32s-14.3 32-32 32z"
            />
          </svg>
        </a>
      </div>
      <div class="text-white text-lg text-center leading-none p-1">
        <div class="font-extrabold">Welcome</div>
        <div class="font-normal">{$userName}</div>
      </div>
      <div class="h-auto w-[.1875rem] bg-black/50" />
    </div>
    <div class="w-3/5 flex flex-row justify-center gap-x-4 h-auto p-1">
      <div class="basis-3/7 font-semibold text-4xl">{month} {day}, {year}</div>

      <div class="h-auto w-[.1875rem] bg-black/50" />

      <div class="basis-3/7 font-semibold text-4xl">{hour}:{minutes}</div>
    </div>
    <div class="w-1/5 h-auto p-1">
      <div class="h-auto w-[.1875rem] bg-black/50" />
    </div>
  </div>
</div>
