<script>
  let weather = null;
  async function getWeather() {
    const response = await fetch(
      `https://api.weatherapi.com/v1/current.json?key=308499a599c9443390d92636240711&q=Istanbul`
    );
    weather = await response.json();
  }
  getWeather();
</script>

<h1>Weather</h1>

{#if weather}
  <h2>Hava Durumu: {weather.current.temp_c}°C</h2>
  <h3>Durum: {weather.current.condition.text}</h3>
{/if}
