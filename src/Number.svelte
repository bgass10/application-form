<script>
  import FaHashtag from "svelte-icons/fa/FaHashtag.svelte";

  export let number;
</script>

<div class="row">
  <div class="icon">
    <FaHashtag />
  </div>
  <input
    bind:value={number}
    type="tel"
    placeholder="(123)-456-7890"
    onkeypress="this.style.width = ((this.value.length + 1) * 9) + 'px';"
  />
</div>

<style>
  .row {
    display: flex;
    margin-top: 25px;
  }
  .icon {
    width: 22px;
    height: 22px;
    color: #b638ff;
    margin-left: 30px;
  }
  input {
    color: white;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    margin-left: 10px;
    width: 110px;
    border-bottom: 2px solid #b638ff;
    text-align: center;
  }
</style>
