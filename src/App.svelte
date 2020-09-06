<script>
  let price = 10.23;
  let tip = 15;
  const formatter = new Intl.NumberFormat("en-US", {
    style: "currency",
    currency: "USD",
  });

  function calculatTip(price, tip) {
    return formatter.format(price * (tip / 100));
  }

  $: calculatedTip = calculatTip(price, tip);
</script>

<style>
  h1,
  h2 {
    text-align: center;
  }
  input#tip {
    width: 100%;
  }
</style>

<div class="container">
  <div class="row">
    <div class="column">
      <h1>Tip Calculator</h1>
    </div>
  </div>
  <div class="row">
    <div class="column">
      <label for="price">Meal Price</label>
      <input
        bind:value={price}
        type="number"
        id="price"
        placeholder="Total"
        min="0" />
      <label for="tip">Tip ({tip}%)</label>
      <input
        bind:value={tip}
        type="range"
        min="0"
        max="100"
        step="1"
        id="tip" />
    </div>
  </div>
  <div class="row">
    <div class="column">
      <h2>Calculated Tip: {calculatedTip}</h2>
    </div>
  </div>
</div>
