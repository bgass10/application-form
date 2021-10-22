<script>
  import IoLogoSnapchat from "svelte-icons/io/IoLogoSnapchat.svelte";

  export let snapchat;
</script>

<div class="row">
  <div class="icon">
    <IoLogoSnapchat />
  </div>
  <input
    bind:value={snapchat}
    type="text"
    placeholder="snapchatusername"
    onkeypress="this.style.width = ((this.value.length + 1) * 9) + 'px';"
  />
</div>

<style>
  .row {
    display: flex;
    margin-top: 25px;
  }
  .icon {
    width: 24px;
    height: 24px;
    color: #b638ff;
    margin-left: 28px;
  }
  input {
    color: white;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
    background-color: #131313;
    border: 0px;
    margin-left: 10px;
    width: 150px;
    border-bottom: 2px solid #b638ff;
    text-align: center;
  }
</style>
