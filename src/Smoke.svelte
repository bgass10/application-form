<script>
  export let smokeVal;
</script>

<div class="col shift">
  <h1>Smoke?</h1>
  <select bind:value={smokeVal}>
    <option>Never</option>
    <option>Rarely</option>
    <option>Sometimes</option>
    <option>Often</option>
  </select>
</div>

<style>
  .col {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  select {
    margin-top: 10px;
    color: #a8a8a8;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    width: 110px;
    text-align: center;
  }
</style>
