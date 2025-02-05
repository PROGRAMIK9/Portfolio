<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte";
  import Header from "../components/Header.svelte";
  let y;
  let innerHeight = 0;
  let innerWidth = 0;

  function gotoTop() {
    document.body.scrollIntoView();
  }
</script>

<div
  class="relative flex flex-col p-0 w-full text-sm sm:text-base min-h-screen"
>
  <div
    class={"fixed bottom-0 right-0 duration-200 flex p-10 z-[10] " +
      (y > 0 ? "opacity-full pointer-events-auto" : "opacity-0 pointer-events-none")}
  >
    <!-- svelte-ignore a11y_consider_explicit_label -->
    <button onclick={gotoTop} class="ml-auto rounded-full bg-slate-700 text-violet-700 px-3 sm:px-4 hover:bg-amber-50 cursor-pointer">
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square"></i>
    </button>
  </div>
  <Header y={y} />
  <slot />
  <Footer />
</div>

<svelte:window bind:innerWidth bind:innerHeight bind:scrollY={y} />
