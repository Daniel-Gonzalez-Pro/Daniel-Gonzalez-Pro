<!DOCTYPE html>
<!-- saved from url=(0047)https://portfolio-demo-1-lime.vercel.app/#about -->
<html lang="en" class="dark"><link type="text/css" rel="stylesheet" id="dark-mode-custom-link"><link type="text/css" rel="stylesheet" id="dark-mode-general-link"><style lang="en" type="text/css" id="dark-mode-custom-style"></style><style lang="en" type="text/css" id="dark-mode-native-style"></style><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"><meta name="viewport" content="width=device-width"><link rel="icon" type="image/webp" href="./PortfolioDemo1_files/logo.webp"><meta name="generator" content="Astro v5.2.5"><title>PortfolioDemo1</title><!-- Metas --><meta name="description" content="A small minimalist web developer portfolio built with Astro and TailwindCSS"><link rel="stylesheet" href="./PortfolioDemo1_files/index.BGWxbwRs.css"><style type="text/css" id="operaUserStyle"></style><style type="text/css"></style></head> <body class="dark:bg-gray-950"> <img class="fixed top-0 left-0 size-full -z-10 blur-2xl" src="./PortfolioDemo1_files/background.BPKAcmfN.svg" alt="" fetchpriority="high"> <header class="max-w-screen-lg mx-auto flex flex-wrap justify-between py-1 px-4 sm:px-6 items-center sticky top-0 z-50 lg:rounded-b-md border border-gray-300 dark:border-neutral-800 backdrop-blur-xs"> <a href="https://portfolio-demo-1-lime.vercel.app/"> <img src="./PortfolioDemo1_files/logo.webp" alt="Logo" title="Logo" aria-label="Logo" loading="eager" width="64" height="64" decoding="async" class="size-16 object-contain object-center bg-transparent"> </a> <div class="sm:order-2 flex items-center gap-3 text-gray-900"> <button title="Theme Toggle" aria-label="Theme Toggle" id="theme-toggle" class="flex items-center gap-2 dark:text-white"> <svg id="theme-sun-icon" class="size-5" aria-label="Sun Icon" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"> </svg> <svg id="theme-moon-icon" class="size-5 hidden" aria-label="Moon Icon" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"> <path d="M223.5 32C100 32 0 132.3 0 256S100 480 223.5 480c60.6 0 115.5-24.2 155.8-63.4c5-4.9 6.3-12.5 3.1-18.7s-10.1-9.7-17-8.5c-9.8 1.7-19.8 2.6-30.1 2.6c-96.9 0-175.5-78.8-175.5-176c0-65.8 36-123.1 89.3-153.3c6.1-3.5 9.2-10.5 7.7-17.3s-7.3-11.9-14.3-12.5c-6.3-.5-12.6-.8-19-.8z"></path></svg> </button> <button title="Navbar Toggle" aria-label="Navbar Toggle" id="navbar-toggle" class="sm:hidden dark:text-white"> <svg aria-label="Menu Icon" id="navbar-menu-icon" class="size-5" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"> <path d="M0 96C0 78.3 14.3 64 32 64l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 128C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 288c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32L32 448c-17.7 0-32-14.3-32-32s14.3-32 32-32l384 0c17.7 0 32 14.3 32 32z"></path></svg> <svg aria-label="Close Menu Icon" id="navbar-x-icon" class="hidden size-6" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"> <path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"></path></svg> </button> </div> <nav id="navbar" class="hidden -translate-y-[200%] transition-transform p-4 sm:block sm:translate-y-0 sm:static sm:p-0 w-full sm:w-auto text-sm lg:text-base"> <ul class="flex flex-col items-center gap-4 lg:gap-6 border border-dashed border-gray-500 rounded-md font-semibold text-gray-500 p-4 sm:p-2 sm:border-none sm:bg-transparent sm:flex-row"> <li> <a href="https://portfolio-demo-1-lime.vercel.app/#home" class="hover:text-gray-950 dark:hover:text-white dark:text-gray-400"> Proyectos </a> </li><li>  </li><li> </li><li> </li> </ul> </nav> </header> <script>
  const navbar = document.getElementById("navbar");
  const navbarToggle = document.getElementById("navbar-toggle");
  const navbarXIcon = document.getElementById("navbar-x-icon");
  const navbarMenuIcon = document.getElementById("navbar-menu-icon");

  if (navbarToggle instanceof HTMLButtonElement) {
    navbarToggle.addEventListener("click", () => {
      navbarXIcon.classList.toggle("hidden");
      navbarMenuIcon.classList.toggle("hidden");

      navbar.classList.toggle("hidden");

      setTimeout(() => {
        navbar.classList.toggle("-translate-y-[200%]");
      });
    });
  }

  const themeToggle = document.getElementById("theme-toggle");
  const themeMoonIcon = document.getElementById("theme-moon-icon");
  const themeSunIcon = document.getElementById("theme-sun-icon");

  const isDarkColorThemeSet =
    "color-theme" in localStorage &&
    localStorage.getItem("color-theme") === "dark";
  const userPrefersDarkTheme =
    window.matchMedia("(prefers-color-scheme: dark)").matches &&
    !("color-theme" in localStorage);

  if (isDarkColorThemeSet || userPrefersDarkTheme) {
    setDarkTheme();
  } else {
    setLightTheme();
  }

  if (themeToggle instanceof HTMLButtonElement) {
    themeToggle.addEventListener("click", () => {
      const colorTheme = localStorage.getItem("color-theme");

      if (colorTheme === "dark") {
        setLightTheme();
      } else {
        setDarkTheme();
      }
    });
  }

  function setLightTheme() {
    document.documentElement.classList.remove("dark");
    localStorage.setItem("color-theme", "light");

    themeMoonIcon.classList.remove("hidden");
    themeSunIcon.classList.add("hidden");
  }

  function setDarkTheme() {
    localStorage.setItem("color-theme", "dark");
    document.documentElement.classList.add("dark");

    themeMoonIcon.classList.add("hidden");
    themeSunIcon.classList.remove("hidden");
  }
</script> <main class="max-w-screen-lg mx-auto p-6 flex flex-col gap-12">  <section id="home" class="flex flex-col"> <article class="text-gray-950 dark:text-white text-pretty mx-auto"> <h1 class="text-4xl md:text-6xl font-bold max-w-screen-sm text-center">
Portafolio Daniel González



</h1> <div class="flex flex-col gap-6 mt-8"> <h2 class="font-bold text-xl sm:text-2xl text-center">

<div class="h-14"></div>
Ingeniero de Ejecución en Informática
</h2> 


<main class="max-w-screen-lg mx-auto p-6 flex flex-col gap-12">
  <section id="home" class="flex flex-col">
    <article class="text-gray-950 dark:text-white text-pretty mx-auto">

      <!-- Título principal -->
      <h1 class="text-4xl md:text-6xl font-bold max-w-screen-sm text-center">
        
      </h1>

      <!-- Espacio vacío entre títulos -->
      <div class="h-2"></div>

      <!-- Subtítulo separado -->
      <h2 class="font-bold text-xl sm:text-2xl text-center">
       
      </h2>

    </article>
  </section>
</main>





<div class="flex flex-col sm:flex-row gap-4 overflow-hidden relative"> <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 card">  <div class="rounded-full p-4 grid place-content-center bg-blue-50 text-blue-500 dark:bg-blue-950/30 dark:text-blue-700 w-fit"> <svg class="size-8" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512"><path d="M128 32C92.7 32 64 60.7 64 96l0 256 64 0 0-256 384 0 0 256 64 0 0-256c0-35.3-28.7-64-64-64L128 32zM19.2 384C8.6 384 0 392.6 0 403.2C0 445.6 34.4 480 76.8 480l486.4 0c42.4 0 76.8-34.4 76.8-76.8c0-10.6-8.6-19.2-19.2-19.2L19.2 384z"></path></svg> </div> <h2 class="font-semibold text-lg sm:text-xl md:text-2xl">
Lenguajes de Programación
</h2> <p class="text-gray-600 text-sm sm:text-base dark:text-gray-400">
C, C#, Python, SQL

</p>  </div> <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 card">  <div class="rounded-full p-4 grid place-content-center bg-yellow-50 text-yellow-500 dark:bg-yellow-950/30 dark:text-yellow-700 w-fit"> <svg class="size-8" fill="currentColor" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M64 32C28.7 32 0 60.7 0 96l0 64c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-64c0-35.3-28.7-64-64-64L64 32zm280 72a24 24 0 1 1 0 48 24 24 0 1 1 0-48zm48 24a24 24 0 1 1 48 0 24 24 0 1 1 -48 0zM64 288c-35.3 0-64 28.7-64 64l0 64c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-64c0-35.3-28.7-64-64-64L64 288zm280 72a24 24 0 1 1 0 48 24 24 0 1 1 0-48zm56 24a24 24 0 1 1 48 0 24 24 0 1 1 -48 0z"></path></svg> </div> <h2 class="font-semibold text-lg sm:text-xl md:text-2xl">
Ciberseguridad
</h2> <p class="text-gray-600 text-sm sm:text-base dark:text-gray-400">
Bootcamp Fundamentos de Ciberseguridad
             
</p>  </div> </div> </div> </article> </section> <section id="about" class="flex flex-col"> <h2 class="text-2xl md:text-4xl font-bold text-gray-950 dark:text-white mb-8">
Acerca de mi
</h2> <article class="flex flex-col md:flex-row gap-4 p-4"> <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 text-gray-600 dark:text-gray-400 h-fit">  <div class="flex flex-col gap-2 text-sm sm:text-base"> <h3 class="text-lg sm:text-xl font-semibold text-gray-950 dark:text-white">
Biografía 
</h3> <p>
Mi nombre es Daniel Gonzalez, talquino de nacimiento, soy Ingeniero Informático
			formado en la Universidad Católica del Maule.
</p> <p>
He trabajado en modalidad Freelance con distintos clientes con diferentes niveles de conocimientos informáticos, a los que he asesorado e implementado soluciones. También me desempeñé en el área informática de una clínica odontológica.
</p> <p>
Mi correo para contacto es d.elias2040@hotmail.com 
</p> </div> <div class="flex flex-col gap-2"> <h3 class="text-lg sm:text-xl font-semibold text-gray-950 dark:text-white">

</h3>  </div>  </div> <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 p-8">  <ol class="relative border-s border-gray-300 dark:border-neutral-800"> <li class="mb-10 ms-8"> <span class="absolute flex items-center justify-center size-6 bg-blue-300 rounded-full -start-3 ring-8 ring-blue-100 dark:ring-blue-950/60 dark:bg-blue-800"> <div class="size-full p-1"><svg class="size-4 text-gray-600 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"> <path stroke-linecap="round" stroke-width="2" d="M8 8V6a2 2 0 012-2h4a2 2 0 012 2v2"></path> <path stroke-linecap="round" stroke-width="2" d="M4 14l3.15.787a20 20 0 009.7 0L20 14"></path> <path stroke-linejoin="round" stroke-width="2" d="M4 10a2 2 0 012-2h12a2 2 0 012 2v8a2 2 0 01-2 2H6a2 2 0 01-2-2v-8z"></path><circle cx="12" cy="12" r="1"></circle></svg></div> 
</span> <h3 class="flex items-center mb-1 text-lg font-semibold text-gray-950 dark:text-white"> UCM </h3> <time class="block mb-2 text-sm font-normal leading-none text-gray-500"> 2008-2014 Ingeniería de Ejecución en Informática</time>
 <p class="mb-4 text-sm sm:text-base font-normal text-gray-600 dark:text-gray-400">  </p> 
 </li><li class="mb-10 ms-8"> <span class="absolute flex items-center justify-center size-6 bg-blue-300 rounded-full -start-3 ring-8 ring-blue-100 dark:ring-blue-950/60 dark:bg-blue-800"> <div class="size-full p-1"><svg class="size-4  text-gray-600 dark:text-gray-400" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
 <path d="M19 1C19 0.447715 19.4477 0 20 0C20.5523 0 21 0.447715 21 1V1.58582L22.2709 0.314894C22.6614 -0.0756305 23.2946 -0.0756294 23.6851 0.314895C24.0757 0.705419 24.0757 1.33858 23.6851 1.72911L22.4142 3H23C23.5523 3 24 3.44772 24 4C24 4.55228 23.5523 5 23 5H20.4142L12.7017 12.7125C12.3112 13.103 11.678 13.103 11.2875 12.7125C10.897 12.322 10.897 11.6888 11.2875 11.2983L19 3.58582V1Z"></path><path d="M17.3924 3.78908C17.834 3.3475 17.7677 2.61075 17.2182 2.31408C15.6655 1.47581 13.8883 1 12 1C5.92487 1 1 5.92487 1 12C1 18.0751 5.92487 23 12 23C18.0751 23 23 18.0751 23 12C23 10.1154 22.5261 8.34153 21.6909 6.79102C21.3946 6.24091 20.6574 6.17424 20.2155 6.61606L20.1856 6.64598C19.8554 6.97615 19.8032 7.48834 20.016 7.90397C20.6451 9.1326 21 10.5249 21 12C21 16.9706 16.9706 21 12 21C7.02944 21 3 16.9706 3 12C3 7.02944 7.02944 3 12 3C13.4782 3 14.8732 3.35638 16.1037 3.98791C16.5195 4.20129 17.0322 4.14929 17.3627 3.81884L17.3924 3.78908Z"></path><path d="M14.3899 6.79159C14.8625 6.31902 14.7436 5.52327 14.1062 5.32241C13.4415 5.11295 12.7339 5 12 5C8.13401 5 5 8.13401 5 12C5 15.866 8.13401 19 12 19C15.866 19 19 15.866 19 12C19 11.2702 18.8883 10.5664 18.6811 9.9049C18.4811 9.26659 17.6846 9.14697 17.2117 9.61995L17.1194 9.71224C16.8382 9.99337 16.7595 10.4124 16.8547 10.7984C16.9496 11.1833 17 11.5858 17 12C17 14.7614 14.7614 17 12 17C9.23858 17 7 14.7614 7 12C7 9.23858 9.23858 7 12 7C12.4172 7 12.8225 7.0511 13.21 7.1474C13.5965 7.24347 14.0166 7.16496 14.2982 6.88331L14.3899 6.79159Z"></path><path d="M11.078 9.15136C11.4874 9.01484 11.6934 9.48809 11.3882 9.79329L10.5827 10.5989C9.80254 11.379 9.80254 12.6438 10.5827 13.4239C11.3628 14.204 12.6276 14.204 13.4077 13.4239L14.2031 12.6285C14.5089 12.3227 14.9822 12.5301 14.8429 12.9397C14.441 14.1209 13.3135 15 12 15C10.3431 15 9 13.6569 9 12C9 10.6796 9.88827 9.54802 11.078 9.15136Z"></path></svg></div>
 </span> <h3 class="flex items-center mb-1 text-lg font-semibold text-gray-950 dark:text-white"> Curso de Desarrollo en Python  </h3> <time class="block mb-2 text-sm font-normal leading-none text-gray-500"> </time> <p class="mb-4 text-sm sm:text-base font-normal text-gray-600 dark:text-gray-400">  2021 </p>  </li>
 
 <li class="mb-10 ms-8"> <span class="absolute flex items-center justify-center size-6 bg-blue-300 rounded-full -start-3 ring-8 ring-blue-100 dark:ring-blue-950/60 dark:bg-blue-800"> <div class="size-full p-1"><svg class="size-4 text-gray-600 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"> <path stroke-linecap="round" stroke-width="2" d="M8 8V6a2 2 0 012-2h4a2 2 0 012 2v2"></path> <path stroke-linecap="round" stroke-width="2" d="M4 14l3.15.787a20 20 0 009.7 0L20 14"></path> <path stroke-linejoin="round" stroke-width="2" d="M4 10a2 2 0 012-2h12a2 2 0 012 2v8a2 2 0 01-2 2H6a2 2 0 01-2-2v-8z"></path><circle cx="12" cy="12" r="1"></circle></svg></div> </span> 
<h3 class="flex items-center mb-1 text-lg font-semibold text-gray-950 dark:text-white"> Bootcamp Fundamentos de Ciberseguridad  </h3> <time class="block mb-2 text-sm font-normal leading-none text-gray-500"> 2025</time>

 </li> </ol>  </div> </article> </section> <section id="projects" class="flex flex-col">








<main class="max-w-screen-lg mx-auto p-6 flex flex-col gap-12">
  <section id="home" class="flex flex-col">
    <article class="text-gray-950 dark:text-white text-pretty mx-auto">
      <div class="flex flex-col gap-6 mt-8">
        <div class="flex flex-col sm:flex-row gap-4 overflow-hidden relative">

          <!-- 🔹 Tarjeta: Lenguajes de Programación -->
          <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 card">
            <h2 class="font-semibold text-lg sm:text-xl md:text-2xl">
              INTERESES
            </h2>
            <p class="text-gray-600 text-sm sm:text-base dark:text-gray-400">
              Mis intereses incluyen la tecnología, el hardware de PC, ajedrez, ciclismo de montaña, motociclismo y actividades físicas como senderismo, ping pong.  También disfrutar de la música en Alta Fidelidad
            </p>
          </div>

          <!-- 🔹 Tarjeta: Ciberseguridad -->
          <div class="rounded-md p-6 w-full border border-gray-300 dark:border-neutral-800 flex flex-col gap-2 bg-white shadow-sm dark:bg-gray-950/30 card">
            <h2 class="font-semibold text-lg sm:text-xl md:text-2xl">
              BUSQUEDA PROFESIONAL
            </h2>
            <p class="text-gray-600 text-sm sm:text-base dark:text-gray-400">
              Como Ingeniero Informático en formacion en Ciberseguridad, estoy en búsqueda de oportunidades para aplicar mis conocimientos en implementación de políticas de Ciberseguridad, gestión de incidentes y análisis de vulnerabilidades. 
Puedo adaptarme a modalidades tanto presencial como remoto, Freelance o fijo.
Me interesa cualquier sector que esté en la etapa de implementación y adecuación de sus normas respecto a las nuevas leyes recientemente implementadas sobre Ciberseguridad en el país  
            </p>
          </div>

        </div>
      </div>
    </article>
  </section>
</main>









 <h2 class="text-2xl md:text-4xl font-bold text-gray-950 dark:text-white  text-center mb-8">
 

Proyectos de Ciberseguridad
</h2> <div class="p-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6"> <a href="https://gotosend.com/" target="_blank" class="relative flex flex-col items-stretch duration-300 ease-out p-3 group h-fit rounded-md bg-white dark:bg-gray-950/30 w-full lg:max-w-82"> <span class="absolute inset-0 z-20 block size-full duration-300 ease-out bg-transparent border border-transparent group-hover:-translate-x-1 group-hover:-translate-y-1 group-hover:border group-hover:border-gray-300 dark:group-hover:border-neutral-800 rounded-md group-hover:bg-white dark:group-hover:bg-gray-950/30"></span> <span class="absolute inset-0 z-10 block w-full h-full duration-300 ease-out border rounded-md border-gray-300 dark:border-neutral-800 group-hover:translate-x-1 group-hover:translate-y-1"></span> <span class="relative z-30 block duration-300 ease-out group-hover:-translate-x-1 group-hover:-translate-y-1"> <span class="block w-full"> <img src="./PortfolioDemo1_files/gotosend.webp" loading="lazy" alt="GotoSend" width="200" height="200" decoding="async" class="w-full max-h-72 rounded-lg object-center object-cover"> </span> <span class="block w-full px-1 mt-5 mb-1 sm:mt-3"> <span class="flex items-center mb-0 text-base font-semibold tracking-tight text-gray-950 dark:text-gray-100"> <span>NOMBRE DEL PROYECTO</span> <svg class="group-hover:translate-x-0 group-hover:translate-y-0 -rotate-45 translate-y-1 -translate-x-1 w-2.5 h-2.5 stroke-current ml-1 transition-all ease-in-out duration-200 transform" viewBox="0 0 13 15" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"><g id="svg" transform="translate(0.666667, 2.333333)" stroke="currentColor" stroke-width="2.4"><g><polyline class="transition-all duration-200 ease-out opacity-0 delay-0 group-hover:opacity-100" points="5.33333333 0 10.8333333 5.5 5.33333333 11"></polyline><line class="transition-all duration-200 ease-out transform -translate-x-1 opacity-0 group-hover:translate-x-0 group-hover:opacity-100 group-hover:ml-0" x1="10.8333333" y1="5.5" x2="0.833333333" y2="5.16666667"></line></g></g></g></svg> </span> <span class="text-sm text-gray-600 dark:text-gray-400 block truncate">Informacion del Proyecto.</span> </span> </span> </a>

</button> </div> </div> <script type="module" src="./PortfolioDemo1_files/ErrorModal.astro_astro_type_script_index_0_lang.DGhXI6EQ.js.descargar"></script> <script type="module" src="./PortfolioDemo1_files/HireServiceModal.astro_astro_type_script_index_0_lang.Hy3VBa-j.js.descargar"></script>  </main> <footer class="rounded-md border border-gray-300 dark:border-neutral-800"> <div class="max-w-screen-lg mx-auto sm:flex sm:items-center sm:justify-between p-4 sm:p-6"> <p class="mb-4 text-sm text-center text-gray-500 dark:text-gray-400 sm:mb-0">
</script></body></html>











<!--
**Daniel-Gonzalez-Pro/Daniel-Gonzalez-Pro** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
