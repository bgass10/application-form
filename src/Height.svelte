<script>
  export let feet;
  export let inches;
</script>

<div class="col shiftX">
  <h1>Height</h1>
  <div class="textRow">
    <input bind:value={feet} placeholder="#" />
    <h2>ft</h2>
    <input bind:value={inches} placeholder="#" />
    <h2>in</h2>
  </div>
</div>

<style>
  .col {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .textRow {
    display: flex;
  }
  input {
    color: white;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    width: 10px;
  }
</style>
