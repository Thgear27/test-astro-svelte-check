<script lang="ts">
  // This enforces svelte 5 usage
  type Props = {
    initialCount: number;
  };

  const { initialCount }: Props = $props();

  let count = $state((() => initialCount)());

  function add() {
    count += 1;
  }
</script>

<div class="card">
  <button onclick={add}>+</button>
  <p>No children prop defined.</p>
</div>
