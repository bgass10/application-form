<script>
  import IoIosAdd from "svelte-icons/io/IoIosAdd.svelte";
  const addArtist = () => {
    artists = [...artists, { name: window.prompt("Enter an artist") }];
  };

  export let artists = [];
</script>

<div class="row">
  <div>
    <h1>Favorite Artists</h1>
  </div>
  <div class="icon" on:click={addArtist}>
    <IoIosAdd />
  </div>
</div>
<div class="row p">
  {#each artists as { name }}
    <div class="wrapper">
      <p>{name}</p>
    </div>
  {/each}
</div>

<style>
  .p {
    margin-left: 15px;
  }
  .row {
    margin-top: 15px;
    display: flex;
    flex-wrap: wrap;
  }
  h1 {
    margin-left: 30px;
  }
  .wrapper {
    background-color: #b638ff;
    padding: 0px 10px;
    margin-left: 15px;
    margin-top: 10px;
    border-radius: 25px;
  }
  .icon {
    color: #b638ff;
    width: 32px;
    height: 32px;
    margin-left: 10px;
    margin-top: 16px;
  }
  .icon:hover {
    color: #131313;
    background-color: #b638ff;
    border-radius: 32px;
  }
  p {
    color: white;
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 14px;
  }
</style>
