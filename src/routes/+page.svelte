<script lang="ts">
  import { ShoppingBag } from "lucide-svelte";
  import { Button } from "$lib/components/ui/button";
  import Navbar from "$lib/components/combined/navbar.svelte";
  import ShowCase from "$lib/components/combined/showcase.svelte";
  // let scroll: number;
</script>

<div class="overflow-x-hidden">
  <Navbar />

  <!-- main page -->
  <div class="relative overflow-x-hidden">
    <!-- bgvideo -->
    <video
      autoplay
      muted
      loop
      playsinline
      class="fixed top-0 left-0 w-full h-full object-cover -z-10 brightness-50"
    >
      <source src="/video_of_women_modelling_1080p.mp4" />
    </video>

    <div class="flex justify-between items-start w-screen h-screen">
      <div
        class="font-serif text-9xl font-extrabold text-amber-200 text-center absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2"
      >
        BELLA ALCHEVI
        <Button
          variant="ghost"
          class="text-amber-200 hover:text-amber-200 bg-slate-900 hover:bg-slate-700"
        >
          <ShoppingBag class="h-4 w-4 ml-1 mr-4 font-sans text-amber-200" />
          SHOP NOW
        </Button>
      </div>
    </div>
  </div>
  <ShowCase model="/model1.webp" title="90s Kick" />
  <ShowCase model="/model3.webp" flow={true} title="La Vistra" />
  <ShowCase model="/model2.webp" title="Winter Fluff" />
</div>
