<script>
  import Form from "./Form.svelte";

  let submitted = false;
</script>

<svelte:head>
  <link
    href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap"
    rel="stylesheet"
  />
</svelte:head>

{#if submitted}
  <div class="containerSubmit">
    <h1 class="congrats">Congratulations!</h1>
    <h2>Your application was successfully submitted.</h2>
  </div>
{:else}
  <Form bind:submitted />
{/if}

<style>
  h2 {
    font-size: 24px;
    text-align: center;
    margin-top: 35px;
  }
</style>
