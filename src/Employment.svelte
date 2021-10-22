<script>
  import IoMdCash from "svelte-icons/io/IoMdCash.svelte";
  export let employment;
</script>

<div class="row">
  <div class="icon">
    <IoMdCash />
  </div>
  <div>
    <h1>Employment</h1>
  </div>
</div>
<input bind:value={employment} placeholder="some form of employment" />

<style>
  .row {
    display: flex;
  }
  h1 {
    margin-left: 10px;
  }
  .icon {
    color: #b638ff;
    width: 26px;
    height: 26px;
    margin-left: 30px;
    margin-top: 20px;
  }
  input {
    color: #a8a8a8;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    margin-left: 30px;
    width: 80%;
    margin-top: 10px;
  }
</style>
