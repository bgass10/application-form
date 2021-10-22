<script>
  import IoIosSchool from "svelte-icons/io/IoIosSchool.svelte";
  export let college;
  export let major;
</script>

<div class="row">
  <div class="icon">
    <IoIosSchool />
  </div>
  <div>
    <h1>Education</h1>
  </div>
</div>
<div class="rowTextLong">
  <input
    bind:value={college}
    placeholder="college or university"
    type="text"
    style="text-align:center"
    onkeypress="this.style.width = ((this.value.length + 1) * 9) + 'px';"
  />
  <h2>, studying&nbsp;</h2>
  <input
    class="right"
    bind:value={major}
    placeholder="major"
    type="text"
    onkeypress="this.style.width = ((this.value.length + 1) * 9) + 'px';"
  />
</div>

<style>
  .rowTextLong {
    display: flex;
    margin-left: 30px;
  }
  .row {
    display: flex;
    margin-top: 0px;
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
    width: 150px;
  }
  .right {
    width: 45px;
  }
</style>
