<script>
  export let title;
</script>

<section class="w-[80%] md:w-[50%] mx-auto pt-10">
  <header>
    <h2 class="dark:text-[#DFDFD6] text-slate-800 text-3xl font-bold">{title}</h2>
  </header>
  <slot />
</section>
