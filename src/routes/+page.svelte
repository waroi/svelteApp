<script>
  import Selam from "../components/Selam.svelte";
  let name1 = "";
  let a = 0;
  let b = 0;
  $: toplam = a + b;
</script>

<h1>Merhaba {name1}</h1>

<input type="text" bind:value={name1} placeholder="Adınızı giriniz" />

<p>A Değeri: <input type="number" bind:value={a} /></p>
<p>B Değeri: <input type="number" bind:value={b} /></p>
<p>Toplam: {toplam}</p>

<Selam name="Varol" />

<style>
  h1 {
    width: 100%;
  }
</style>
