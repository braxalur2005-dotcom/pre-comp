---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cdn.pixabay.com/photo/2024/05/21/19/58/code-8779051_1280.jpg
# some information about your slides (markdown enabled)
title: Compiladores
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-left
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 35min
---

# Compiladores
**Segundo parcial**

<div @click="$slidev.nav.next" class="mt-10 inline-block px-4 py-2 rounded lg border border white/30px" hover:bg="white op-10">
  Iniciar <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>



---
transition: fade-out
layout: two-cols
layoutclass: gap-10
---

# ¿Qué veremos hoy?

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<div class="pt-4 grid gap-4 text-[1.2rem]" style="color:#0A56A3;">
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">01</span>
    <span class="font-800">Introducción y objetivos</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">02</span>
    <span class="font-800">¿Qué es la programación?</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">03</span>
    <span class="font-800">Primeros pasos</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">04</span>
    <span class="font-800">Tipos de lenjuage de programación</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">05</span>
    <span class="font-800">Tipos de operadores y datos</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">06</span>
    <span class="font-800">La importancia de la sintaxis</span>
  </div>
</div>

<style>
/* Mueve el recuadro un poco hacia arriba y muestra la parte superior de la imagen */
.slidev-img-top {
  width: 100%;
  height: calc(100vh - 4rem);
  object-fit: cover;
  object-position: top center;
  display: block;
  border-radius: .75rem;
  box-shadow: 0 10px 30px rgba(0,0,0,0.15);
}

/* Mantiene toda la imagen visible sin recortar */
.slidev-img-contain {
  width: 100%;
  height: calc(100vh - 4rem);
  object-fit: contain;
  object-position: top center;
  display: block;
  border-radius: .75rem;
  box-shadow: 0 8px 24px rgba(0,0,0,0.12);
}

/* Ajustes para pantallas pequeñas */
@media (max-width: 1024px) {
  .slidev-img-top, .slidev-img-contain {
    height: 50vh;
    margin-top: 0;
  }
}
</style>

::right::

 <div class="h-[100%] flex">
  <img src="./components/Img/1.png" alt="Entorno digital" class="slidev-img-top" />
</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-800 tracking-[-0.5px] m-0 mb-6" style="color:#0A56A3;">
  Introducción y objetivos
</h1>

<div class="pt-4 gap-4">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.3rem] leading-relaxed">
    La programación: es el proceso de crear instrucciones para que una computadora realice tareas específicas, dividiendo un problema grande en una serie de pasos lógicos y ordenados, conocidos como algoritmos.
  </p>

  <div class="grid grid-cols-3 gap-10 text-left mt-8 text-[1.05rem]">
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 1</div>
      <div>Saber los <strong>conceptos básicos de programación</strong>.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 2</div>
      <div>Conocer los <strong>tipos de lenjuage de programación</strong>.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 3</div>
      <div>Explicar como funcionan los <strong>operadores</strong> y los tipos.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 4</div>
      <div>Aprenderse <strong>los tipos de datos</strong> que existen en la programación.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 5</div>
      <div>Conocer <strong>la sintaxis de cada lenjuage</strong> que utilizan.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Objetivo 6</div>
      <div>poder dominar los <strong>distintos lenjuages</strong> de programación.</div>
    </div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-800 tracking-[-0.5px] m-0 mb-6" style="color:#0A56A3;">
  ¿Qué es la programación?
</h1>

<div class="pt-4 gap-4">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.3rem] leading-relaxed">
    La programación es el proceso de dar instrucciones a una computadora para que realice tareas específicas.
Esas instrucciones se escriben en un lenguaje de programación, como Python, Java, C++, JavaScript, etc.
  </p>

  <div class="grid grid-cols-2 gap-10 text-left mt-8 text-[1.05rem]">
    
<div v-click class="bg-grey/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Consepto más a fondo</div>
      <div>Es simplemente darle órdenes a una computadora para que haga lo que tú quieras, así como le dirías a alguien “enciende la luz” o “abre la puerta”; en este caso, le dices a la computadora “muestra un mensaje”, “suma estos números” o “guarda este dato”.</div><div>La diferencia es que la computadora no entiende español, por eso usamos lenguajes especiales llamados lenguajes de programación, como Python, JavaScript o C++.</div>
    </div>
    <div class="h-[100%] flex">
  <img src="./components/Img/2.png" alt="Entorno digital" class="h-[100%] w-full object-position: top rounded-xl shadow-xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Primeros pasos
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.3rem] leading-relaxed">
    Los pseudocódigos y diagramas de flujo existen porque ayudan a planear y entender un programa antes de escribirlo en un lenguaje de programación.
  </p>

  <div class="grid grid-cols-2 gap-10 text-left mt-8 text-[1.05rem]">
    
<div v-click class="bg-grey/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Pseudocódigo:</div>
      <div>es una forma de escribir los pasos de un algoritmo usando un lenguaje parecido al humano, pero con una estructura lógica similar a la programación.</div><div><strong>Diagramas de flujo:</strong></div><div>son representaciones gráficas de un algoritmo mediante figuras y flechas que muestran el orden de las operaciones; permiten visualizar el proceso de manera clara y sencilla.</div><div><strong>-Ambos ayudan a diseñar, analizar y comprender cómo funcionará un programa antes de programarlo.</strong></div>
    </div>
    <div class="h-[100%] flex">
  <img src="./components/Img/7.png" alt="Entorno digital" class="h-[100%] w-full object-cover-contein rounded-xl shadow-xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-800 tracking-[-0.5px] m-0 mb-6" style="color:#0A56A3;">
  Tipos de lenjuage de programación
</h1>

<div class="pt-4 gap-4">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.3rem] leading-relaxed">
    Un lenguaje de programación es un sistema de instrucciones que permite comunicarse con la computadora para crear programas, aplicaciones o sistemas que realicen tareas específicas.
  </p>

  <div class="grid grid-cols-2 gap-10 text-left mt-8 text-[1.05rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/4.png" alt="Entorno digital" class="h-[100%] w-full object-cover rounded-xl shadow-xl" style="height: 100vh;" />
</div>
<div v-click class="bg-grey/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Tipos que existen</div>
      <div><strong>Bajo nivel:</strong> cercanos al hardware, muy rápidos pero difíciles (Ej. Assembly).</div><div><strong>Medio nivel:</strong> combinan potencia y control (Ej. C).</div><div><strong>Alto nivel:</strong> fáciles de entender y usar (Ej. Python, Java, C++).</div><div><strong>Web:</strong> crean páginas y sitios web (Ej. HTML, CSS, JavaScript).</div><div><strong>Scripting:</strong> automatizan tareas (Ej. Python, Bash, Ruby).</div><div><strong>Especializados:</strong> usados en áreas específicas (Ej. SQL, R, MATLAB).</div>
    </div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-800 tracking-[-0.5px] m-0 mb-6" style="color:#0A56A3;">
  Tipos de operadores y datos
</h1>

<div class="pt-4 gap-4">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.3rem] leading-relaxed">
    Lo que tienen en común los tipos de datos y los operadores es que ambos son elementos básicos de la programación y trabajan juntos para procesar información dentro de un programa.

Los tipos de datos indican qué clase de información se está usando (números, texto, verdadero o falso), mientras que los operadores sirven para realizar acciones o cálculos con esa información. En resumen, los datos son lo que se usa y los operadores son lo que se hace con ellos.
  </p>

<div class="grid grid-cols-2 gap-10 text-left mt-8 text-[1.05rem]">
<div v-click class="bg-grey/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Tipos de Operadores</div>
      <div>Los operadores son símbolos que se usan para realizar operaciones con los datos, como sumar, comparar o asignar valores. Existen diferentes tipos: los aritméticos, los relacionales, los lógicos y los de asignación.</div>
    </div>
    <div v-click class="bg-grey/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Tipos de Datos</div>
      <div>Los tipos de datos son las diferentes clases de información que puede manejar una computadora, como números, textos o valores lógicos. Sirven para que el programa sepa qué tipo de dato está usando y cómo debe tratarlo.</div>
    </div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  La importancia de la sintaxis
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    La sintaxis es importante porque establece las reglas que determinan cómo deben escribirse correctamente las instrucciones en un lenguaje de programación, permitiendo que la computadora las entienda y las ejecute sin errores; si la sintaxis se usa mal, el programa no funcionará correctamente o no podrá ejecutarse.
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/5.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-contain-cover rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>


---
transition: fade-out
layout: two-cols
layoutclass: gap-10
---

# Siguentes lecciones

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<div class="pt-4 grid gap-4 text-[1.2rem]" style="color:#0A56A3;">
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">01</span>
    <span class="font-800">Tipos de programación</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">02</span>
    <span class="font-800">programación estructurada</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">03</span>
    <span class="font-800">programación orientada a objetos</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">04</span>
    <span class="font-800">programación funcional</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">05</span>
    <span class="font-800">programación lógica</span>
  </div>
  <div class="flex items-baseline gap-2" v-click>
    <span class="font-800" style="font-size:2.2rem; color:#7FD6E5; min-width:3.4ch;">06</span>
    <span class="font-800">Tipos de compiladores</span>
  </div>
</div>

::right::

<div class="h-[100%] flex">
  <img src="./components/Img/1.png" alt="Entorno digital" class="h-[100%] w-full object-cover rounded-xl shadow-xl" style="height: 100vh;" />
</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.5px] m-0 mb-6" style="color:#0A56A3;">
  Tipos de programación
</h1>

<div class="pt-4 gap-4">

<div class="mx-auto max-w-5xl gab-4" style="color:#0A56A3;">
  <p class="text-[1.0rem] leading-relaxed">
    Existen varios tipos de programación porque cada uno está diseñado para resolver diferentes tipos de problemas y adaptarse a distintas formas de pensar y trabajar.por eso existen algunos necesitan rapidez, otros organización, precisión matemática o ejecución simultánea (como estructurado, orientado a objetos o funcional).
  </p>

  <div class="grid grid-cols-3 gap-10 text-left mt-8 text-[1.05rem]">
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">Estructurada:</div>
      <div>organiza el código en bloques con secuencias, condicionales y bucles.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">orientada a objetos:</div>
      <div>usa clases y objetos para modelar elementos del mundo real.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">funcional:</div>
      <div>se basa en funciones matemáticas y evita modificar datos.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">lógica:</div>
      <div>utiliza reglas y hechos para deducir conclusiones.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">declarativa:</div>
      <div>se enfoca en qué se quiere hacer, no en cómo hacerlo.</div>
    </div>
    <div v-click class="bg-white/90 rounded-xl shadow-lg p-5">
      <div class="font-800 mb-1">concurrente:</div>
      <div>permite ejecutar varias tareas al mismo tiempo.</div>
    </div>
  </div> 
</div>

</div>
---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Programación estructurada
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    La programación estructurada es una forma de escribir programas de manera ordenada y lógica, dividiendo el código en partes o bloques que se ejecutan de forma secuencial, con decisiones y repeticiones controladas. Su propósito es mejorar la claridad, reducir errores y facilitar el mantenimiento del programa al evitar el desorden y el uso excesivo de saltos como “goto”.
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/6.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-contain-cover-contein rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>
---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Programación orientada a objetos
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    La programación orientada a objetos (POO) es un tipo de programación que organiza el código en objetos, los cuales representan cosas del mundo real y contienen atributos (datos) y métodos (acciones). Su objetivo es hacer que el código sea más fácil de entender, reutilizar y mantener, ya que permite crear programas basados en la interacción entre objetos, siguiendo principios como herencia, encapsulamiento y polimorfismo.
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/8.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-contain-cover rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>
---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Programación funcional
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    La programación funcional es un tipo de programación que se basa en el uso de funciones matemáticas para resolver problemas, evitando cambiar datos o usar variables globales. En este enfoque, el resultado de una función depende solo de sus entradas, lo que hace el código más predecible, fácil de probar y mantener. Se enfoca en qué se quiere hacer, más que en cómo hacerlo, y es común en lenguajes como Haskell, Lisp o Scala.
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/9.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-contain-cover rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Programación lógica
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    La programación lógica es un tipo de programación que se basa en el razonamiento y las reglas lógicas para resolver problemas. En lugar de indicar paso a paso qué hacer, el programador define hechos y reglas, y el programa utiliza la lógica para deducir conclusiones o respuestas. Este tipo de programación se usa mucho en inteligencia artificial y sistemas expertos, y un lenguaje común para aplicarla es Prolog.
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/10.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-cover rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>

---
transition: fade-out
class: text-center
---

<h1 class="font-600 tracking-[-0.1px] m-0 mb-3" style="color:#0A56A3;">
  Tipos de compiladores
</h1>

<div class="pt-0.5 gap-0.5">

<div class="mx-auto max-w-5xl gab-0.5" style="color:#0A56A3;">
  <p class="text-[1.2rem] leading-relaxed">
    Existen varios tipos de compiladores, entre los principales están: el compilador de una sola pasada, que traduce el código en un solo recorrido; el compilador de varias pasadas, el compilador cruzado, el intérprete, y el compilador JIT (Just In Time), que combina compilación e interpretación para optimizar la ejecución en tiempo real.<div><strong>
    ¡ESTO FUE CREADO CON COMPILADORES!</strong></div>
  </p>
 
  <div class="grid gap-10 text-left mt-8 text-[0.3rem]">
    <div class="h-[100%] flex">
  <img src="./components/Img/11.png" alt="Entorno digital" class="h-[100%] w-auto md:w-auto lg:w-auto object-cover-contein rounded-xl shadow-2xl" style="height: 100vh;" />
</div>
  </div> 
</div>

</div>


---
layout: center
class: text-center
---

# Gracias por su atención

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 45%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

[Inicio](http://localhost:3030/1) · [¿Qué veremos hoy?](http://localhost:3030/2) · [Siguientes lecciones](http://localhost:3030/9)

<PoweredBySlidev mt-10 />
