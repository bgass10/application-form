<script>
  const setPic = () => {
    src =
      window.prompt("Enter image URL") ||
      "https://th.bing.com/th/id/OIP.1Agw8tPi1oidtC_q4U4ZdgHaHa?pid=ImgDet&rs=1";
  };

  export let name;
  export let age;
  export let city;
  export let state;
  export let src;
</script>

<img {src} alt="img" class="center" on:click={setPic} />
<div class="rowText">
  <input
    class="h1 a"
    bind:value={name}
    placeholder="First Last"
    type="text"
    onkeypress="this.style.width = ((this.value.length + 1) * 12) + 'px';"
  />
  <h1>&nbsp;|&nbsp;</h1>
  <input
    class="h1 b"
    bind:value={age}
    placeholder="Age"
    type="text"
    onkeypress="this.style.width = ((this.value.length + 1) * 13) + 'px';"
  />
</div>
<div class="rowText">
  <input
    class="h2 c"
    bind:value={city}
    placeholder="City"
    type="text"
    onkeypress="this.style.width = ((this.value.length + 1) * 10) + 'px';"
  />
  <h2>,&nbsp;</h2>
  <input
    class="h2 d"
    bind:value={state}
    placeholder="State"
    type="text"
    onkeypress="this.style.width = ((this.value.length + 1) * 12) + 'px';"
  />
</div>

<style>
  .a {
    width: 90px;
  }
  .b {
    width: 40px;
  }
  .c {
    width: 30px;
  }
  .d {
    width: 40px;
  }
  .h1 {
    color: white;
    font-size: 18px;
    font-family: Montserrat;
    font-weight: 700;
    margin-top: 20px;
  }
  .h2 {
    color: #a8a8a8;
    font-size: 14px;
    font-family: Montserrat;
    font-weight: 600;
  }
  .rowText {
    display: flex;
    justify-content: center;
  }
  input {
    background-color: #131313;
    border: 0px;
    text-align: center;
  }
  img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    justify-self: center;
    border: 3px solid #b638ff;
  }
  h1,
  h2 {
    text-align: center;
  }
  .center {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
</style>
