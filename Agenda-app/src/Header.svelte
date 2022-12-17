<script>
  import DateSelect from "./Date-select.svelte";
</script>

<div class="header-container">
  <div class="header-content">
    <div class="logo" />
    <DateSelect />
    <div class="format-selection" />
  </div>
</div>

<style>
  .header-container {
    border: 1px solid white;
    width: 100%;
    height: 80px;
    top: 0;
  }

  .header-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .logo {
    background-color: aliceblue;
    height: 80px;
    width: 80px;
  }
  .date-select {
    background-color: aliceblue;
    height: 80px;
    width: 80px;
  }
  .format-selection {
    background-color: aliceblue;
    height: 80px;
    width: 80px;
  }
</style>
