<script>
  import {
    AddSharp,
    ArrowBack,
    ArrowForwardCircleSharp,
    Analytics,
    Apps,
    Bandage,
    BonfireOutline,
    Book,
    Walk,
    WalkOutline,
    WalkSharp,
    Barcode,
    BarcodeSharp,
    BarcodeOutline,
  } from "svelte-ionicons";

  export let size = "2em";
  export let width = size;
  export let height = size;
  export let color = "green";
  export let viewBox = "0 0 24 24";

  let monthName = [
    "January",
    "February",
    "March",
    "April",
    "May",
    "June",
    "July",
    "August",
    "September",
    "October",
    "November",
    "December",
  ];
  let now = new Date();
  let year = now.getFullYear();
  let month = now.getMonth();
  let day = now.getDate();

  if (month == 1) {
    day = 30;
  }

  function next() {
    month++;
    if (month == 12) {
      year++;
      month = 0;
    }
  }
  function previous() {
    if (month == 0) {
      month = 11;
      year--;
    } else {
      month--;
    }
  }
  function prevDay() {
    if (day == 1) {
      day = 32;
      previous();
    }
    day--;
  }
  function nextDay() {
    if (day == 31) {
      day = 0;
      next();
    }
    day++;
  }
</script>

<button on:click={prevDay} />
<p class="date">
  {day}
  {monthName[month]}
  {year}
</p>
<button on:click={nextDay} />

<ArrowForwardCircleSharp
  color="cyan"
  size="40"
  on:click={nextDay}
/>

<style>
  .date {
    color: white;
  }
</style>
