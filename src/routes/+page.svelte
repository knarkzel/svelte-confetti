<script>
  import { tick } from "svelte";
  import { Confetti } from "svelte-confetti";

  let active = false;
  async function showConfetti() {
    active = false;
    await tick();
    active = true;
  }
</script>

<h1>Hello there</h1>
<button on:click={showConfetti}>Show some confetti</button>

{#if active}
  <Confetti infinite amount={200} />
{/if}
