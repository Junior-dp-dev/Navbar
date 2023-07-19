<script>
  import "../app.postcss";
  function Menu() {
    let list = document.querySelector("ul");
    list.classList.toggle("top-[60px]");
    list.classList.toggle("opacity-100");
  }
</script>

<nav class="flex items-center justify-between w-full px-20 gap-10 h-[60px] text-white font-bold text-2xl font-handlee bg-m8-verde-fundo2">
  <div class="flex justify-between items-center w-full">
    <a href="/" class=" text-3xl bg-m8-amarelo rounded-xl px-2 r"> <img src="logo.png" alt="Logo" class="h-8" /></a>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <ion-icon class="md:hidden block text-3xl text-white cursor-pointer" name="menu" on:click={Menu} />
  </div>

  <ul
    class="gap-10 md:flex pl-10 text-white md:items-center md:static absolute bg-m8-verde-fundo2 w-full left-0 md:w-auto md:py-0 pb-6 md:opacity-100 opacity-0 top-[-400px] transition-all ease-in duration-300">
    <li class=" my-6 md:my-0">
      <a href="/tirolesa" class="text-xl hover:text-cyan-500 duration-500">Tirolesa</a>
    </li>
    <li class=" my-6 md:my-0">
      <a href="/cursos" class="text-xl hover:text-cyan-500 duration-500">Cursos</a>
    </li>
    <li class=" my-6 md:my-0">
      <a href="/sobre" class="text-xl hover:text-cyan-500 duration-500">Sobre</a>
    </li>
    <a href="/contato" class="bg-m8-amarelo hover:bg-m8-verde-icons text-white font-bold pb-[0.1rem] px-2 rounded-xl"> Contato </a>
  </ul>
</nav>

<slot />
