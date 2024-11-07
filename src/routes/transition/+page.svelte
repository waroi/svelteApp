<script>
  import { fade } from "svelte/transition";
  let items = [];
  let newItem = "";
</script>

<input type="text" bind:value={newItem} placeholder="Yeni birşey ekle" />
<button on:click={() => (items = [...items, newItem])}>Ekle</button>

<ul>
  {#each items as item (item)}
    <li transition:fade>{item}</li>
  {/each}
</ul>
