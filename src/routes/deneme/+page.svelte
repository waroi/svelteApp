<script>
  import { count, doubleCount } from "../../store/store";
</script>

<h1>Sayaç: {$count}</h1>

<button on:click={() => ($count += 1)}>Arttır</button>

<h1>İki Katı: {$doubleCount}</h1>
