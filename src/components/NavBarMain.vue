<template>
    <div class="flex justify-between bg-zinc-800 px-4 pr-1 py-2 items-center text-white sm:pr-5">
      <div class="">
        <img src="../assets/logo2.png" alt="Logo" class="w-16 h-16 rounded-circle">
      </div>
      <nav class="hidden lg:w-1/2 md:flex md:w-2/3">
        <ul class="flex justify-between px-5 w-full">
          <li class="hover:underline hover:scale-105 transition-all duration-200 text-emerald-400">
            <a href="#" class="font-bold text-xl tracking-wide">Home</a>
          </li>
          <li class="hover:underline hover:scale-105 transition-all duration-200 text-emerald-400">
            <a href="#" class="font-bold text-xl tracking-wide">About</a>
          </li>
          <li class="hover:underline hover:scale-105 transition-all duration-200 text-emerald-400">
            <a href="#" class="font-bold text-xl tracking-wide">Contact</a>
          </li>
        </ul>
      </nav>

      <div class="">
            <a
              href="#"
              class="hidden md:inline-block rounded-lg px-5 py-2 text-xl font-semibold leading-5 text-slate-100 ring-1 ring-slate-100/70 hover:ring-slate-100/20"
              >Log In</a
            >
          </div>

          <div class="icon mr-3 md:hidden">
            <svg version="1.1" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="#abb">
            <title>list2</title>
            <path d="M12 2h20v4h-20v-4zM12 14h20v4h-20v-4zM12 26h20v4h-20v-4zM0 4c0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.209-1.791 4-4 4s-4-1.791-4-4zM0 16c0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.209-1.791 4-4 4s-4-1.791-4-4zM0 28c0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.209-1.791 4-4 4s-4-1.791-4-4z"></path>
</svg>
          </div>
    </div>
</template>