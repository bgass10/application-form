<script>
  import Height from "./Height.svelte";
  import Religion from "./Religion.svelte";
  import Drink from "./Drink.svelte";
  import Smoke from "./Smoke.svelte";

  export let feet;
  export let inches;
  export let religion;
  export let drinkVal;
  export let smokeVal;
</script>

<div class="rowMobile">
  <Height bind:feet bind:inches />
  <Religion bind:religion />
  <Drink bind:drinkVal />
  <Smoke bind:smokeVal />
</div>

<style>
</style>
