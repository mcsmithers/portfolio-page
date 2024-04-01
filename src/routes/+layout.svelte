<script>
  import "../app.css";
	import Footer from "../components/Footer.svelte";
	import Header from "../components/Header.svelte";

  let y;
  let innerHeight = 0
  let innerWidth = 0

  function goToTop() {
    document.body.scrollIntoView()
  }
</script>

<div class="realtive flex flex-col max-w[1440px] mx-auto w-full text-sm sm:text-bas min-h-screen">
  <div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10]" + (
      y > 0 ? ' opactiy-full pointer-events-auto' :  ' pointer-events-none opacity-0'
    )}>
    <button on:click={goToTop} class="ml-auto rounded-full bg-slaate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
      <i class="fa-solid fa-arrow-up grid place-items-center aspect-square"></i>
    </button>
  </div>
  <Header y={y}/>
  <slot />
  <Footer/>
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth/>


