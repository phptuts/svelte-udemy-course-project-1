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
      <input type="number" id="price" placeholder="Total" min="0" />
      <label for="tip">Tip (15%)</label>
      <input type="range" min="0" max="100" step="1" id="tip" />
    </div>
  </div>
  <div class="row">
    <div class="column">
      <h2>Calculated Tip: $12.00</h2>
    </div>
  </div>
</div>
