<script>
  // @ts-nocheck

  import CalendarContent from "./Calendar-content.svelte";
  import Header from "./Header.svelte";
  import MiniCalendar from "./Mini-calendar.svelte";
</script>

<main>
  <body>
    <Header />
    <div class="blocs">
      <MiniCalendar />
      <CalendarContent />
    </div>
  </body>
</main>

<style>
  .blocs {
    display: flex;
    flex-direction: row;
    width: 100%;
    gap: 20px;
  }
</style>
