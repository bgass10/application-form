<script>
  export let religion;
</script>

<div class="col">
  <h1>Religion</h1>
  <div class="textRow">
    <input class="smallText" bind:value={religion} placeholder="..." />
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
    margin-top: 10px;
  }
  input {
    color: #a8a8a8;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    width: 100px;
    text-align: center;
  }
</style>
