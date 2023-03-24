<script>
  import { fade } from 'svelte/transition';
  
  let isVisible = true;
  
  function toggleVisibility() {
    isVisible = !isVisible;
  }
</script>

<button on:click={toggleVisibility}>Toggle Visibility</button>

{#if isVisible}
  <div transition:fade={{ duration: 500, delay: 100, opacity: 0.5 }}>Hello, world!</div>
{/if}