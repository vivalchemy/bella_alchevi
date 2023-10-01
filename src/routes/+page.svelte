<script>
  import { ShoppingBag, ShoppingCart } from 'lucide-svelte';
  import { Button } from "$lib/components/ui/button";
</script>

<div class="flex justify-between items-start w-screen " >
  <div class="relative top-6 left-4">
    <Button variant="ghost" class="underline underline-offset-4">Contact Us</Button>
  </div> 
  <div class="font-serif text-9xl text-center absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2">BELLA ALCHEVI</div>
  
<div class="flex flex-nowrap relative top-6 right-4">
  <Button variant="ghost">
    <ShoppingBag class="h-4 w-4 mx-1" />
    Bag
  </Button>
  
  <Button variant="ghost" on:click>
    <ShoppingCart class="h-4 w-4 mx-1"/>
    Cart
  </Button>
</div>
  
</div>