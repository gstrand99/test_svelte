<script>
  import DesktopHeader from "$lib/components/DesktopHeader.svelte";
  import DesktopFooter from "$lib/components/DesktopFooter.svelte";
</script>

<div class="flex flex-col p-1 h-screen">
  <div class="justify-self-start">
    <DesktopHeader />
  </div>
  <div class="justify-self-end">
    <DesktopFooter />
  </div>
</div>
