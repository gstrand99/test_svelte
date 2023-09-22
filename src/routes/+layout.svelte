<script>
  import "../app.postcss";
  import wallpaper from "$lib/assets/wallpaper.webp";
</script>

<div
  class="font-sans bg-cover bg-center bg-no-repeat h-screen overflow-hidden"
  style="background-image: url({wallpaper});"
>
  <slot />
</div>
