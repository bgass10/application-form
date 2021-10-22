<script>
  import IoLogoInstagram from "svelte-icons/io/IoLogoInstagram.svelte";

  export let instagram;
</script>

<div class="row">
  <div class="icon">
    <IoLogoInstagram />
  </div>
  <input
    bind:value={instagram}
    type="text"
    placeholder="instagramhandle"
    onkeypress="this.style.width = ((this.value.length + 1) * 9) + 'px';"
  />
</div>

<style>
  .row {
    display: flex;
    margin-top: 25px;
  }
  .icon {
    width: 26px;
    height: 26px;
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
    width: 130px;
    border-bottom: 2px solid #b638ff;
    text-align: center;
  }
</style>
