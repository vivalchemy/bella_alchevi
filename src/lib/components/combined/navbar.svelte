<script lang="ts">
  import { ShoppingBag, ShoppingCart } from "lucide-svelte";
  import { Button } from "$lib/components/ui/button";
  let scroll: number;
</script>

<svelte:window bind:scrollY={scroll} />

<div class="fixed w-screen h-fit flex px-8 pt-6 justify-between items-center">
  <Button
    variant="ghost"
    class=" bg-slate-900 underline underline-offset-4 text-amber-200 hover:text-amber-200 hover:bg-slate-700"
    >Contact Us</Button
  >
  {#if scroll > 480}
    <Button
      variant="ghost"
      class="font-serif text-2xl transition text-amber-200 hover:text-amber-200 hover:bg-slate-700 bg-slate-900"
    >
      BELLA ALCHEVI
    </Button>
  {/if}

  <div class="flex rounded-md bg-slate-900">
    <Button
      variant="ghost"
      class="text-amber-200 hover:text-amber-200 hover:bg-slate-700 "
    >
      <ShoppingBag class="h-4 w-4 mx-1" />
      Bag
    </Button>

    <Button
      variant="ghost"
      class="text-amber-200 hover:text-amber-200 hover:bg-slate-700"
    >
      <ShoppingCart class="h-4 w-4 mx-1" />
      Cart
    </Button>
  </div>
</div>