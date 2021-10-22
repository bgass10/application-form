<script>
  import IoIosAdd from "svelte-icons/io/IoIosAdd.svelte";
  const addHobby = () => {
    hobbies = [...hobbies, { desc: window.prompt("Enter a hobby") }];
  };

  export let hobbies = [];
</script>

<div class="row">
  <div>
    <h1>Hobbies</h1>
  </div>
  <div class="icon" on:click={addHobby}>
    <IoIosAdd />
  </div>
</div>
<div class="row p">
  {#each hobbies as { desc }}
    <div class="wrapper">
      <p>{desc}</p>
    </div>
  {/each}
</div>

<style>
  .p {
    margin-left: 15px;
  }
  .row {
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
