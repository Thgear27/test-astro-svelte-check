<script lang="ts">
  import type { Snippet } from "svelte";

  type Props = {
    children?: Snippet;
  };

  const { children }: Props = $props();
</script>

<div class="card">
  {#if children}
    {@render children()}
  {:else}
    <p>No content provided.</p>
  {/if}
</div>
