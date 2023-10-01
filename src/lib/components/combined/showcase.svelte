<script lang="ts">
  export let model = "default";
  export let title: string = "default";
  export let description: string = "default";
  export let flow: boolean = false;
  import { Button } from "$lib/components/ui/button";
  let width: number;
  let height: number;
</script>

<svelte:window bind:innerHeight={height} bind:innerWidth={width} />

{#if flow === false}
  <div
    class="h-screen flex sm:flex-wrap justify-between items-center py-32 px-60 bg-black text-amber-200"
  >
    {#if width > height}
      <img
        src={model}
        alt=""
        srcset=""
        class="w-auto h-full object-contain min-w-430"
      />
    {:else}
      <img src={model} alt="" srcset="" class="h-auto w-full object-contain" />
    {/if}
    <div class="flex flex-col items-center justify-center">
      <div class="font-serif text-start text-6xl py-16">{title}</div>
      <Button>View Collection</Button>
    </div>
  </div>
{:else}
<div
class="h-screen flex flex-row-reverse sm:flex-wrap justify-between items-center py-32 px-60 bg-black text-amber-200"
>
{#if width > height}
  <img
    src={model}
    alt=""
    srcset=""
    class="w-auto h-full object-contain min-w-430"
  />
{:else}
  <img src={model} alt="" srcset="" class="h-auto w-1/2 object-contain" />
{/if}
<div class="flex flex-col items-center justify-center">
  <div class="font-serif text-start text-6xl py-16">{title}</div>
  <Button>View Collection</Button>
</div>
</div>
{/if}
