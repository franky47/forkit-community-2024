---
theme: geist
background: false
title: Maintaining an open-source library for Next.js
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
class: text-center
highlighter: shiki
drawings:
  persist: false
mdc: true
transition: fade
defaults:
  layout: center
layout: cover
---

# Maintaining an open-source library for Next.js

<p class="font-medium">Feedback & tips</p>

<footer class="flex items-end justify-between fixed bottom-4 left-4 right-4">
  <div class="flex items-center gap-4 justify-center">
    <img src="/img/47ng.svg" width="48" height="48" class="bg-white rounded-full p-0.5 w-16 h-16 dark:w-12 dark:h-12"/>
    <div class="text-left">
      <div class="text-2xl text-primary font-semibold">
        François Best
      </div>
      <div>
        @fortysevenfx
      </div>
    </div>
  </div>
  <div class="text-right">
    <img src="/img/forkit-logo-light.svg" width="200" class="dark:hidden" />
    <img src="/img/forkit-logo-dark.svg" width="200" class="hidden dark:block" />
    <div class="mt-1 font-semibold">Rouen 2024</div>
  </div>
</footer>

<!--
This talk is called...
-->

---
title: Thanks to the sponsors
class: bg-white
---

<img src="/img/sponsors/bearstudio@web.png" class="h-64 mx-auto" />

<div class="flex gap-x-8 flex-wrap justify-center">
  <img src="/img/sponsors/attineos@web.png" class="h-32" />
  <img src="/img/sponsors/magnolia@web.png" class="h-32" />
  <img src="/img/sponsors/docaposte-agility@web.png" class="h-32" />
  <img src="/img/sponsors/oneprepaid@web.png" class="h-32" />
  <img src="/img/sponsors/le-village-by-ca@web.png" class="h-32" />
  <img src="/img/sponsors/digit@web.png" class="h-32" />
</div>

<!--
First, thanks to the sponsors & Bear Studio for inviting me

This is my first talk at a tech conference

so please bear with me.
-->

---
title: Light/dark
---

<LightOrDark>
  <template #light>
    <h1 class="text-9xl text-center">Light mode</h1>
  </template>
  <template #dark>
    <h1 class="text-9xl text-center">Dark mode</h1>
  </template>
</LightOrDark>


---
title: What to expect
---

<h1 class="text-9xl text-center">What to expect</h1>

<!--
No Next.js or React experience required

Web standards

Web app behaviours & best practices
-->


---
title: Hello!
---

<div class="flex items-center gap-8 justify-center">
  <img src="/img/47ng.svg" width="128" height="128" class="bg-white rounded-full p-0.5 w-42 h-42 dark:w-38 dark:h-38"/>
  <div class="text-left space-y-2">
    <div class="text-7xl text-primary font-semibold">
      François Best
    </div>
    <div class="text-5xl text-zinc-500 font-medium">
      @fortysevenfx
    </div>
  </div>
</div>

<div class="flex justify-center mt-10">
  <div class="p-4 bg-white inline-block">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 29 29" class="size-48"><path fill="#ffffff" d="M0,0 h29v29H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM8 0h1v1H8zM11 0h1v1H11zM13 0h1v1H13zM17 0h2v1H17zM20 0h1v1H20zM22,0 h7v1H22zM0 1h1v1H0zM6 1h1v1H6zM9 1h1v1H9zM11 1h3v1H11zM15 1h3v1H15zM19 1h1v1H19zM22 1h1v1H22zM28,1 h1v1H28zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM9 2h2v1H9zM14 2h2v1H14zM18 2h3v1H18zM22 2h1v1H22zM24 2h3v1H24zM28,2 h1v1H28zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM9 3h1v1H9zM12 3h1v1H12zM15 3h5v1H15zM22 3h1v1H22zM24 3h3v1H24zM28,3 h1v1H28zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM8 4h1v1H8zM10 4h1v1H10zM13 4h3v1H13zM19 4h1v1H19zM22 4h1v1H22zM24 4h3v1H24zM28,4 h1v1H28zM0 5h1v1H0zM6 5h1v1H6zM8 5h3v1H8zM13 5h3v1H13zM18 5h1v1H18zM20 5h1v1H20zM22 5h1v1H22zM28,5 h1v1H28zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22,6 h7v1H22zM9 7h5v1H9zM15 7h2v1H15zM19 7h2v1H19zM1 8h7v1H1zM10 8h2v1H10zM13 8h4v1H13zM18 8h2v1H18zM23 8h2v1H23zM28,8 h1v1H28zM0 9h2v1H0zM4 9h2v1H4zM7 9h1v1H7zM10 9h6v1H10zM22 9h5v1H22zM28,9 h1v1H28zM1 10h2v1H1zM4 10h1v1H4zM6 10h1v1H6zM8 10h2v1H8zM20 10h4v1H20zM25 10h2v1H25zM0 11h2v1H0zM3 11h2v1H3zM7 11h3v1H7zM21 11h3v1H21zM25 11h1v1H25zM27 11h1v1H27zM0 12h2v1H0zM4 12h1v1H4zM6 12h2v1H6zM21 12h1v1H21zM23 12h1v1H23zM26,12 h3v1H26zM1 13h4v1H1zM7 13h1v1H7zM19 13h4v1H19zM24 13h2v1H24zM27,13 h2v1H27zM2 14h2v1H2zM5 14h2v1H5zM8 14h2v1H8zM20 14h2v1H20zM23 14h1v1H23zM0 15h1v1H0zM2 15h1v1H2zM4 15h2v1H4zM8 15h2v1H8zM19 15h2v1H19zM24 15h2v1H24zM28,15 h1v1H28zM0 16h1v1H0zM3 16h1v1H3zM5 16h2v1H5zM9 16h1v1H9zM20 16h1v1H20zM23 16h1v1H23zM25 16h3v1H25zM0 17h1v1H0zM9 17h1v1H9zM19 17h1v1H19zM22 17h1v1H22zM24,17 h5v1H24zM0 18h1v1H0zM2 18h1v1H2zM4 18h3v1H4zM8 18h1v1H8zM20 18h1v1H20zM22 18h1v1H22zM24 18h2v1H24zM0 19h1v1H0zM2 19h4v1H2zM7 19h3v1H7zM11 19h2v1H11zM15 19h1v1H15zM20 19h1v1H20zM22 19h1v1H22zM27,19 h2v1H27zM0 20h1v1H0zM3 20h2v1H3zM6 20h1v1H6zM8 20h8v1H8zM17 20h1v1H17zM19 20h6v1H19zM26,20 h3v1H26zM8 21h1v1H8zM10 21h2v1H10zM13 21h1v1H13zM18 21h1v1H18zM20 21h1v1H20zM24 21h2v1H24zM27,21 h2v1H27zM0 22h7v1H0zM8 22h1v1H8zM11 22h2v1H11zM15 22h2v1H15zM18 22h3v1H18zM22 22h1v1H22zM24 22h1v1H24zM0 23h1v1H0zM6 23h1v1H6zM8 23h2v1H8zM12 23h3v1H12zM16 23h1v1H16zM19 23h2v1H19zM24 23h2v1H24zM27,23 h2v1H27zM0 24h1v1H0zM2 24h3v1H2zM6 24h1v1H6zM8 24h3v1H8zM12 24h1v1H12zM14 24h2v1H14zM18 24h1v1H18zM20 24h7v1H20zM28,24 h1v1H28zM0 25h1v1H0zM2 25h3v1H2zM6 25h1v1H6zM8 25h1v1H8zM10 25h8v1H10zM19 25h3v1H19zM23 25h1v1H23zM25 25h2v1H25zM0 26h1v1H0zM2 26h3v1H2zM6 26h1v1H6zM8 26h1v1H8zM17 26h1v1H17zM19 26h9v1H19zM0 27h1v1H0zM6 27h1v1H6zM8 27h1v1H8zM12 27h2v1H12zM16 27h1v1H16zM18 27h4v1H18zM24 27h2v1H24zM27 27h1v1H27zM0 28h7v1H0zM13 28h1v1H13zM17 28h1v1H17zM21 28h2v1H21zM24 28h3v1H24z" shapeRendering="crispEdges"></path><image href="/img/x.svg" height="7.25" width="7.25" x="10.875" y="10.875" preserveAspectRatio="none"/></svg>
  </div>
</div>

<!--
My name is François Best

Find me on X (formerly Twitter) as @fortysevenfx.
-->

---
title: What I do
---

<p class="text-center text-black dark:text-white text-6xl font-bold">Freelance web developer</p>

<div class="grid grid-cols-5 items-center justify-center gap-x-12 gap-y-4 text-center text-3xl text-zinc-500 mt-20">
  <img src="/img/typescript.svg" alt="Fastify" class="w-32 h-32" />
  <img src="/img/react.svg" alt="React" class="w-32 h-32" />
  <img src="/img/next.svg" alt="Next.js" class="w-32 h-32" />
  <img src="/img/nodejs.svg" alt="Node.js" class="w-32 h-32" />
  <img src="/img/fastify-dark.svg" alt="Fastify" class="w-32 h-32 hidden dark:block" />
  <img src="/img/fastify-light.svg" alt="Fastify" class="w-32 h-32 block dark:hidden" />
  <label>TypeScript</label>
  <label>React</label>
  <label>Next.js</label>
  <label>Node.js</label>
  <label>Fastify</label>
</div>

<div class="flex justify-center mt-10">
  <div class="p-4 bg-white inline-block">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 29 29" class="size-32"><path fill="#ffffff" d="M0,0 h29v29H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM8 0h1v1H8zM11 0h1v1H11zM13 0h1v1H13zM17 0h2v1H17zM20 0h1v1H20zM22,0 h7v1H22zM0 1h1v1H0zM6 1h1v1H6zM9 1h1v1H9zM11 1h3v1H11zM15 1h3v1H15zM19 1h1v1H19zM22 1h1v1H22zM28,1 h1v1H28zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM9 2h2v1H9zM14 2h2v1H14zM18 2h3v1H18zM22 2h1v1H22zM24 2h3v1H24zM28,2 h1v1H28zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM9 3h1v1H9zM12 3h1v1H12zM15 3h5v1H15zM22 3h1v1H22zM24 3h3v1H24zM28,3 h1v1H28zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM8 4h1v1H8zM10 4h1v1H10zM13 4h3v1H13zM19 4h1v1H19zM22 4h1v1H22zM24 4h3v1H24zM28,4 h1v1H28zM0 5h1v1H0zM6 5h1v1H6zM8 5h3v1H8zM13 5h3v1H13zM18 5h1v1H18zM20 5h1v1H20zM22 5h1v1H22zM28,5 h1v1H28zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22,6 h7v1H22zM9 7h5v1H9zM15 7h2v1H15zM19 7h2v1H19zM1 8h7v1H1zM10 8h2v1H10zM13 8h4v1H13zM18 8h2v1H18zM23 8h2v1H23zM28,8 h1v1H28zM0 9h2v1H0zM4 9h2v1H4zM7 9h1v1H7zM10 9h6v1H10zM22 9h5v1H22zM28,9 h1v1H28zM1 10h2v1H1zM4 10h1v1H4zM6 10h1v1H6zM8 10h2v1H8zM20 10h4v1H20zM25 10h2v1H25zM0 11h2v1H0zM3 11h2v1H3zM7 11h3v1H7zM21 11h3v1H21zM25 11h1v1H25zM27 11h1v1H27zM0 12h2v1H0zM4 12h1v1H4zM6 12h2v1H6zM21 12h1v1H21zM23 12h1v1H23zM26,12 h3v1H26zM1 13h4v1H1zM7 13h1v1H7zM19 13h4v1H19zM24 13h2v1H24zM27,13 h2v1H27zM2 14h2v1H2zM5 14h2v1H5zM8 14h2v1H8zM20 14h2v1H20zM23 14h1v1H23zM0 15h1v1H0zM2 15h1v1H2zM4 15h2v1H4zM8 15h2v1H8zM19 15h2v1H19zM24 15h2v1H24zM28,15 h1v1H28zM0 16h1v1H0zM3 16h1v1H3zM5 16h2v1H5zM9 16h1v1H9zM20 16h1v1H20zM23 16h1v1H23zM25 16h3v1H25zM0 17h1v1H0zM9 17h1v1H9zM19 17h1v1H19zM22 17h1v1H22zM24,17 h5v1H24zM0 18h1v1H0zM2 18h1v1H2zM4 18h3v1H4zM8 18h1v1H8zM20 18h1v1H20zM22 18h1v1H22zM24 18h2v1H24zM0 19h1v1H0zM2 19h4v1H2zM7 19h3v1H7zM11 19h2v1H11zM15 19h1v1H15zM20 19h1v1H20zM22 19h1v1H22zM27,19 h2v1H27zM0 20h1v1H0zM3 20h2v1H3zM6 20h1v1H6zM8 20h8v1H8zM17 20h1v1H17zM19 20h6v1H19zM26,20 h3v1H26zM8 21h1v1H8zM10 21h2v1H10zM13 21h1v1H13zM18 21h1v1H18zM20 21h1v1H20zM24 21h2v1H24zM27,21 h2v1H27zM0 22h7v1H0zM8 22h1v1H8zM11 22h2v1H11zM15 22h2v1H15zM18 22h3v1H18zM22 22h1v1H22zM24 22h1v1H24zM0 23h1v1H0zM6 23h1v1H6zM8 23h2v1H8zM12 23h3v1H12zM16 23h1v1H16zM19 23h2v1H19zM24 23h2v1H24zM27,23 h2v1H27zM0 24h1v1H0zM2 24h3v1H2zM6 24h1v1H6zM8 24h3v1H8zM12 24h1v1H12zM14 24h2v1H14zM18 24h1v1H18zM20 24h7v1H20zM28,24 h1v1H28zM0 25h1v1H0zM2 25h3v1H2zM6 25h1v1H6zM8 25h1v1H8zM10 25h8v1H10zM19 25h3v1H19zM23 25h1v1H23zM25 25h2v1H25zM0 26h1v1H0zM2 26h3v1H2zM6 26h1v1H6zM8 26h1v1H8zM17 26h1v1H17zM19 26h9v1H19zM0 27h1v1H0zM6 27h1v1H6zM8 27h1v1H8zM12 27h2v1H12zM16 27h1v1H16zM18 27h4v1H18zM24 27h2v1H24zM27 27h1v1H27zM0 28h7v1H0zM13 28h1v1H13zM17 28h1v1H17zM21 28h2v1H21zM24 28h3v1H24z" shapeRendering="crispEdges"></path><image href="/img/x.svg" height="7.25" width="7.25" x="10.875" y="10.875" preserveAspectRatio="none"/></svg>
  </div>
</div>

<!--
I'm a freelance web developer since 2018.

Mostly front-end with TypeScript, React & Next.js

Sometimes full-stack with Node.js & Fastify

Before that...
 -->

---
title: Before that (studio)
layout: image
image: /img/ssl.jpg
backgroundSize: fit
---

<!--
I used to work in the audio industry where we turned analog recording studio gear like this...
-->

---
title: Before that (VMR)
layout: image
image: /img/vmr.jpg
backgroundSize: 120vh
class: bg-black
---

<!-- ...into digital plugins using C++ -->

---
title: Native code
---

<h1 class="text-9xl text-center">Native code</h1>

<!-- Native code has drawbacks -->

---
title: Drawbacks of native
---

<div class="text-black dark:text-white text-7xl font-medium leading-relaxed">

- <span class="text-zinc-500">1.</span> Install
- <span class="text-zinc-500">2.</span> Update <small class="text-zinc-500">(manually)</small>
- <span class="text-zinc-500">3.</span> 😓

</div>

<!--
Gatekeeper stores
-->

---
title: In 2016
---

<h1 class="text-7xl -mt-12 mb-12 text-center">2016</h1>

<div class="grid grid-cols-3 gap-x-20 gap-y-2 text-3xl text-center">
  <img src="/img/angular-js.png" class="size-48 block mx-auto"/>
  <img src="/img/vue.svg" class="size-48 block mx-auto"/>
  <img src="/img/react.svg" class="size-48 block mx-auto"/>
  <span>AngularJS</span>
  <span>Vue 1</span>
  <span>React 16<br/><span class="text-zinc-500 text-base">(with Class Components)</span></span>
</div>

<!--
I started using web technologies 8 years ago,
<br/>
when these started to become popular.

Building fast & shipping faster
-->

---
title: Beauty of the web
---

<div class="text-black dark:text-white text-7xl font-medium leading-relaxed">

- <span class="text-zinc-500">1.</span> `git push`
- <span class="text-zinc-500">2.</span> Visit the website
- <span class="text-zinc-500">3.</span> 😍

</div>

<!--
Deploy

Instantly get to the latest version

From anywhere
-->

---
title: The URL
---

<h1 class="text-8xl leading-15">The URL</h1>
<p class="text-zinc-500 text-4xl">The web's superpower</p>

<p class="text-4xl mt-12 font-medium">
  <span class="text-cyan-600 dark:text-cyan-400">https://</span>
  <span class="text-blue-600 dark:text-blue-400">example.com</span>
  <span class="text-green-600 dark:text-green-400">/pathname</span>
  <span class="text-pink-600 dark:text-pink-400">?query=string</span>
  <span class="text-orange-600 dark:text-orange-400">#fragment</span>
</p>

<!--
-> We can..
-->

---
title: What we can do with URLs
---

<div class="text-black dark:text-white text-7xl font-medium leading-relaxed">

- Share them
- Bookmark them
- Navigate history

</div>

---
title: Deep linking
---

<h1 class="text-9xl text-center">Deep Linking</h1>

<p class="text-6xl text-center mt-8 -mb-8 font-semibold" v-click>in web apps?</p>

<!--
Native has deep linking

How can we do it in web apps too?

-> We can leverage parts of the URL
-->

---
title: Pathname
---

<p class="text-6xl">
  <!-- <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span> -->
  <span class="text-green-600 dark:text-green-400 font-semibold">/pathname</span>
  <span class="text-zinc-500">?query=string</span>
  <span class="text-zinc-500">#fragment</span>
</p>

<!--
Content, what page we are on
-->

---
title: Routing in frameworks
---

<h1 class="text-8xl text-center">In Next.js</h1>

<div class="grid grid-cols-2 gap-x-12 text-5xl text-black dark:text-white font-medium items-baseline">
  <p class="text-end">URL pathname</p>
  <p class="font-mono text-3xl font-semibold"><span class="text-zinc-500">https://...</span>/foo/bar</p>
  <p class="text-end">File (pages router)</p>
  <p class="font-mono text-3xl font-semibold">./pages/foo/bar.tsx</p>
  <p class="text-end">File (app router)</p>
  <p class="font-mono text-3xl font-semibold">./app/foo/bar/page.tsx</p>
</div>

<!--
Next.js has two ways of mapping a file name to the URL pathname
-->

---
title: Fragment
---

<p class="text-6xl">
  <!-- <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span> -->
  <span class="text-zinc-500">/pathname</span>
  <span class="text-zinc-500">?query=string</span>
  <span class="text-orange-600 dark:text-orange-400 font-semibold">#fragment</span>
</p>

<!--
Location
-->

---
title: ID scrolling
---

<p class="text-6xl mb-16">
  <!-- <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span> -->
  <span class="text-zinc-500">/a-long-list</span>
  <span class="text-orange-600 dark:text-orange-400 font-semibold">#item-12345</span>
</p>

```html
<ul>
  <!-- lots of items... -->
  <li id="item-12345">Scroll to me!</li>
  <!-- ...lots more items -->
</ul>
```

<style>
pre, code {
  font-size: 2rem;
}
</style>

---
title: The Query string
---

<p class="text-6xl">
  <!-- <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span> -->
  <span class="text-zinc-500">/pathname</span>
  <span class="font-semibold text-black dark:text-white">?<span class="text-pink-600 dark:text-pink-400">query</span>=<span class="text-sky-600 dark:text-sky-400">string</span>
  </span>
  <span class="text-zinc-500">#fragment</span>
</p>

<p class="text-center text-5xl mt-16 -mb-16 text-black dark:text-white" v-click>
query string, search params, query params?
</p>

<!--
Key value store

No consensus on the name

[DEMO] GitHub tabs

-> Story time: back in the pandemic
-->

---
title: Woodworking
layout: image
image: /img/mallet.jpeg
backgroundSize: contain
class: bg-white
---

<!--
During the pandemic, I got into woodworking
-->

---
title: Dovetail designer
layout: image
image: /img/dovetail-light.png
backgroundSize: contain
class: bg-white
---

<!--
I built this little app

[DEMO]

Design on laptop, workshop with my phone

Never used it

Kept reusing the pattern
-->

---
title: Query string in Next.js
---

<h1 class="text-5xl font-bold text-black dark:text-white text-center mt-0 mb-8">In Next.js</h1>

```tsx
import { useSearchParams, useRouter } from 'next/navigation'

function useSearchParamsState(key: string) {
  const searchParams = useSearchParams()
  const router = useRouter()
  const set = (value: string) => {
    const usp = new URLSearchParams(searchParams)
    usp.set(key, value)
    router.replace(`?${usp.toString()}`)
  }
  return [searchParams.get(key), set]
}
```

<style>
pre, code {
  font-size: 1.4rem;
}
</style>

<!--
Verbose

Imperative, error-prone
-->

---
title: next-usequerystate
---

<h1 class="text-5xl font-bold text-black dark:text-white text-center mt-0 mb-8">next-usequerystate</h1>

```tsx
import { useQueryState } from 'next-usequerystate'

function SearchComponent() {
  const [state, setState] = React.useState('')
  const [search, setSearch] = useQueryState('search')
  return (
    <input
      type="search"
      value={search}
      onChange={e => setSearch(e.target.value)}
    />
  )
}
```

<style key="zddqd">
pre, code {
  font-size: 1.4rem;
}
</style>

<!--
Published on NPM

That was in 2020

API looks like React.useState

How useState works: in-memory, lost on page reload

[DEMO] landing
-->

---
title: Users
---

<h1 class="text-6xl text-center mb-12 -mt-8">Used by</h1>

<svg aria-label="Vercel" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 284 65" class="fill-black dark:fill-white mx-auto h-20 mb-6">
  <path d="M141.68 16.25c-11.04 0-19 7.2-19 18s8.96 18 20 18c6.67 0 12.55-2.64 16.19-7.09l-7.65-4.42c-2.02 2.21-5.09 3.5-8.54 3.5-4.79 0-8.86-2.5-10.37-6.5h28.02c.22-1.12.35-2.28.35-3.5 0-10.79-7.96-17.99-19-17.99zm-9.46 14.5c1.25-3.99 4.67-6.5 9.45-6.5 4.79 0 8.21 2.51 9.45 6.5h-18.9zm117.14-14.5c-11.04 0-19 7.2-19 18s8.96 18 20 18c6.67 0 12.55-2.64 16.19-7.09l-7.65-4.42c-2.02 2.21-5.09 3.5-8.54 3.5-4.79 0-8.86-2.5-10.37-6.5h28.02c.22-1.12.35-2.28.35-3.5 0-10.79-7.96-17.99-19-17.99zm-9.45 14.5c1.25-3.99 4.67-6.5 9.45-6.5 4.79 0 8.21 2.51 9.45 6.5h-18.9zm-39.03 3.5c0 6 3.92 10 10 10 4.12 0 7.21-1.87 8.8-4.92l7.68 4.43c-3.18 5.3-9.14 8.49-16.48 8.49-11.05 0-19-7.2-19-18s7.96-18 19-18c7.34 0 13.29 3.19 16.48 8.49l-7.68 4.43c-1.59-3.05-4.68-4.92-8.8-4.92-6.07 0-10 4-10 10zm82.48-29v46h-9v-46h9zM37.59.25l36.95 64H.64l36.95-64zm92.38 5l-27.71 48-27.71-48h10.39l17.32 30 17.32-30h10.39zm58.91 12v9.69c-1-.29-2.06-.49-3.2-.49-5.81 0-10 4-10 10v14.8h-9v-34h9v9.2c0-5.08 5.91-9.2 13.2-9.2z"
  />
</svg>

<div style="width: 90%;" class="mx-auto">
<img src="/img/users-light.png" alt="Users" class="block dark:hidden"/>
<img src="/img/users-dark.png" alt="Users" class="hidden dark:block"/>
</div>

<!--
It got some attention

Vercel, authors of Next.js

Little, but growing community of users and contributors
-->

---
title: Star history
layout: image
image: /img/star-history.png
backgroundSize: contain
class: bg-white
---

<!--
Started talking more about this pattern

-> Earlier this year...
-->

---
title: nuqs
---

<h1 class="text-[180px] font-bold">
  <span class="text-zinc-400 dark:text-zinc-600 font-light">?</span>
  <span>n</span>
  <span class="text-zinc-400 dark:text-zinc-600 font-light">=</span>
  <span>u</span>
  <span class="text-zinc-400 dark:text-zinc-600 font-light">&</span>
  <span>q</span>
  <span class="text-zinc-400 dark:text-zinc-600 font-light">=</span>
  <span>s</span>
</h1>

<!--
Renamed it to nuqs

Next / nuxt / nuqs

-> My goals for it...
-->

---
title: My goals for nuqs
---

<ul class="text-5xl text-black dark:text-white font-semibold space-y-8">
  <li>Works everywhere <span class="text-zinc-500">(pages & app router)</span></li>
  <li>Reliable</li>
  <li>Type-safe</li>
  <li>Server & client</li>
</ul>

<!--
Most modern versions of Next.js

Provide the missing pieces for working with URL state in Next.js

-> One challenge was...
-->

---
title: RSC
---

<h1 class="text-7xl text-center">React Server Components</h1>

---
title: Server-first
---

<h1 class="text-9xl text-center">Server-first</h1>

<!--
Go through the server for every event

Terrible user experience
-->

---
title: Shallow routing
---

<h1 class="text-9xl text-center">Shallow routing</h1>

<!--
Updating the URL without calling the server
-->

---
title: Shallow in nuqs
---

```tsx
// Next.js pages router
router.replace('?new=url', { shallow: true })

// Local-first
useQueryState('q', { shallow: true })

// Server-first
useQueryState('q', { shallow: false })
```

<style key="12">
pre, code {
  font-size: 2rem;
}
</style>

<!--
How to make it work with app router ?
-->

---
title: History API
---

<h1 class="text-9xl text-center">History API</h1>

---
title: Push/replace state
---

```tsx
history.pushState(state, '', url)
history.replaceState(state, '', url)
```

<style key="11">
pre, code {
  font-size: 2.25rem;
}
</style>

<!--
We don't care about state -> move it into the URL to be shared

-> But there's a problem...
-->

---
title: Rate limits
---

<h1 class="text-9xl text-center">Rate limits</h1>

<!--
Define MDN
-->

---
title: Browsers
---

<div class="grid text-7xl font-semibold gap-x-12 gap-y-16 items-center text-black dark:text-white" style="grid-template-columns: 1fr 72px 1fr">
  <span class="justify-self-end">
    Chrome
  </span>
    <img src="/img/chrome.svg" class="inline-block size-18"/>
  <span class="text-green-600 dark:text-green-400">50ms</span>
  <span class="justify-self-end">
    Firefox
  </span>
    <img src="/img/firefox.svg" class="inline-block size-18"/>
  <span class="text-green-600 dark:text-green-400">50ms</span>
  <span class="justify-self-end">
    Safari
  </span>
    <img src="/img/safari.svg" class="inline-block size-18"/>
  <span class="text-amber-600 dark:text-amber-400">120ms 😱</span>
</div>


---
title: Throttling
---

<h1 class="text-9xl text-center">Throttling</h1>

---
title: How throttling works
---

<LightOrDark>
  <template #light>
    <img src="/img/throttling-light.png"/>
  </template>
  <template #dark>
    <img src="/img/throttling-dark.png"/>
  </template>
</LightOrDark>


---
title: Writing
---

<h1 class="text-9xl text-center">State &nbsp;→&nbsp; URL</h1>


---
title: Reading
---

<h1 class="text-9xl text-center">URL &nbsp;→&nbsp; State</h1>


---
title: Parsing
---

<h1 class="text-9xl text-center">Parsing</h1>

---

```tsx
parseAsInteger() // ?int=47
parseAsBoolean() // ?bool=true
parseAsIsoDateTime() // ?date=2024-06-07T09:20:00Z

// Type-safe specific values
const sort = ['asc', 'desc'] as const
parseAsStringLiteral(sort)

// Make your own!
createParser({
  parse() { ... },
  serialize() { ... }
})
```

<style>
pre, code {
  font-size: 1.4rem;
}
</style>

---
title: Reasons for URL changes
---

<h1 class="text-7xl text-center mb-18 -mt-12">The URL changes on…</h1>

<ul class="text-5xl text-black dark:text-white font-semibold space-y-8">
<li>Initial load</li>
<li>Client-side navigation</li>
<li>Third party History updates</li>
<li><code>nuqs</code> updates</li>
</ul>

---
title: useSearchParams
---

<h1 class="text-7xl text-center">useSearchParams()</h1>

---
title: useSearchParams not reactive in older Next
---

<h1 class="text-8xl text-center"><span class="text-zinc-500 font-medium">(was)</span> not reactive 😭</h1>

---
title: Patching globals
---

<h1 class="text-8xl text-center">Patching history 😱</h1>

---

```tsx
history.pushState(state, '', url)
```

<style>
pre, code {
  font-size: 2.5rem;
}
</style>

---
title: Hacking history
---

```tsx
history.pushState(state, 'nuqs_internal', url)

patched_pushState(state, unused, url) {
  if (unused !== 'nuqs_internal') {
    // External URL change
  }
  original_pushState(state, '', url)
}
```

<style>
pre, code {
  font-size: 2rem;
}
</style>

---
title: But why?
---

<h1 class="text-8xl text-center">But why? 🤔</h1>

---
title: Parsers can be expensive
---

<ul class="text-5xl text-black dark:text-white font-semibold space-y-8">
<li>Parsers can be expensive</li>
<li>Parsing on every change is wasteful</li>
<li>We already have the JS values!</li>
</ul>


---
title: Sync
---

<h1 class="text-9xl text-center leading-tight">Syncing via<br/>Event Emitter</h1>

---
title: Sync from URL
---

<img src="/img/sync-light.png" class="block dark:hidden"/>
<img src="/img/sync-dark.png" class="hidden dark:block"/>


---
title: Bug on canary
---

<img src="/img/canary.png" class="h-32 mx-auto"/>

<blockquote class="italic text-6xl">"I have a bug with Next.js <strong>canary</strong>"</blockquote>

---
title: MIT license
---

```
THE SOFTWARE IS PROVIDED "AS IS",
WITHOUT WARRANTY OF ANY KIND
```

<style>
pre, code {
  font-size: 2.5rem;
}
</style>

---
title: What I like
---

<div class="text-black dark:text-white text-6xl font-semibold leading-relaxed">

- <span class="text-zinc-500">1.</span> Install
- <span class="text-zinc-500">2.</span> It just works
- <span class="text-zinc-500">3.</span> 😍

</div>

---
title: Subscribe to Next.js releases
---

<LightOrDark>
  <template #light>
    <img src="/img/sub-release-light.png"/>
  </template>
  <template #dark>
    <img src="/img/sub-release-dark.png"/>
  </template>
</LightOrDark>

---
title: Too many releases
---

<LightOrDark>
  <template #light>
    <img src="/img/next-releases-light.png"/>
  </template>
  <template #dark>
    <img src="/img/next-releases-dark.png"/>
  </template>
</LightOrDark>

---
title: What are our options?
---

<h1 class="text-8xl text-center leading-tight">What are<br/>our options?</h1>

---
title: GitHub API
---

<h1 class="text-6xl text-center mt-0 mb-4">GitHub API</h1>

```json
// GET https://api.github.com/repos/vercel/next.js/releases
[
  {
    "name": "v15.0.0-canary.14",
    "prerelease": true,
    "published_at": "2024-06-05T23:31:15Z",
    "body": "### Core Changes\n\n- Fix loading navigation with metadata..."
  },
  {
    "name": "v15.0.0-canary.13",
    "prerelease": true,
    "published_at": "2024-06-05T21:23:01Z",
    "body": "### Core Changes\n\n- Re-land Fix broken HTML inlining of ..."
  },
  {
    "name": "v15.0.0-canary.12",
    "prerelease": true,
    "published_at": "2024-06-05T03:37:31Z",
    "body": "### Core Changes\n\n- fix NextRequest proxy in edge runtime..."
  },
]
```

<!-- <style key="sqdqqdzddqzm">
pre,code {
  font-size: 0.8rem;
}
</style> -->

---
title: Cron
---

<h1 class="text-8xl text-center flex items-center gap-2"><img src="/img/raspberry-pi.svg" class="h-32 -mt-6 inline-block"/> Cron &nbsp;→&nbsp; CI <img src="/img/gha.svg" class="h-32 inline-block ml-4"/></h1>

---
title: Testing
---

<h1 class="text-9xl text-center">🧪&nbsp; Testing</h1>

---
title: Good tests are the only way to stay sane
---

<blockquote class="text-8xl text-center italic font-bold text-black dark:text-white leading-tight"><span class="text-zinc-500">"</span>Good tests are<br/>the only way<br/>to stay sane<span class="text-zinc-500">"</span></blockquote>

---
title: Behaviour coverage
---

<h1 class="text-9xl text-center"><strike class="text-zinc-500 font-medium">code</strike> behaviour coverage</h1>

---
title: Next.js knobs
---

<div class="text-black dark:text-white text-5xl font-semibold leading-relaxed">

- App vs pages routers
- Static vs \[dynamic\] pages
- `basePath`
- Shallow routing <span class="text-zinc-500 italic">(experimental, then GA)</span>

</div>

---
title: Mocking won't help
layout: image
image: /img/yoda.png
backgroundSize: cover
class: flex items-end justify-center
---

<h1 class="text-6xl text-center text-white">YOUR MOCKS,<br/> YOU WILL NOT NEED THEM</h1>

<style>
  h1 {
    text-shadow: -2px  2px 0 #000,
                  2px  2px 0 #000,
                  2px -2px 0 #000,
                 -2px -2px 0 #000;
  }
</style>

---
title: Golden rule of testing
---

<h1 class="text-9xl text-center leading-tight">Golden rule<br/>of testing</h1>

---

<blockquote class="p-12 text-6xl text-center italic font-medium text-black dark:text-white leading-tight"><span class="text-zinc-500">"</span>A test must fail if, and only if, the <span class="font-extrabold">intention</span> behind the system is not met.<span class="text-zinc-500">"</span></blockquote>

<p class="text-right mr-10 text-4xl text-black dark:text-white leading-tight font-medium">Artem Zakharchenko<br/><a href="https://x.com/kettanaito">@kettanaito</a></p>

---
title: Depending on internals
---

<h1 class="text-9xl text-center leading-tight">Depending on internals</h1>

---
title: Beyoncé rule of software
---

<h1 class="text-9xl text-center leading-tight">Beyoncé rule<br/>of software</h1>

---
title: If you like it then you shoulda put a test on it
layout: image
image: /img/beyonce.jpg
backgroundSize: cover
class: flex items-end justify-center
---

<h1 class="text-6xl text-center text-white leading-tight">IF YOU LIKE IT THEN YOU<br/>SHOULD'VE PUT A TEST ON IT</h1>

<style>
  h1 {
    text-shadow: -2px  2px 0 #000,
                  2px  2px 0 #000,
                  2px -2px 0 #000,
                 -2px -2px 0 #000;
  }
</style>

---
title: End-to-end testing
---

<h1 class="text-8xl text-center leading-tight">
End-to-end testing
  <img src="/img/cypress-light.svg" class="h-32 block dark:hidden mx-auto mt-8"/>
  <img src="/img/cypress-dark.svg" class="h-32 hidden dark:block mx-auto mt-8"/>
</h1>

<!--
This helped me found some issues in the app router core

Did you know ? <next slide>
-->

---
title: App router Redux
---

<h1 class="text-center flex items-center gap-24">
  <img src="/img/next.svg" class="h-48 block"/>
  <span class="text-8xl">❤️</span>
  <img src="/img/redux.svg" class="h-48 block"/>
</h1>

<!--
Redux is still a valid choice for library code

Not so much for application code (feature creep)
-->

---
title: Test matrix
layout: two-cols
---

<LightOrDark>
<template #light>
<img src="/img/matrix-light.png"/>
</template>
<template #dark>
<img src="/img/matrix-dark.png"/>
</template>
</LightOrDark>

::right::

<h1 class="text-7xl text-center leading-tight">Testing<br/>every<br/>supported<br/>version</h1>

<p class="text-center text-zinc-500 text-4xl font-semibold mt-20">With variants</p>


---
title: Thanks Turborepo
---

<svg class="h-48 mr-12" fill="none" viewBox="0 0 120 28" xmlns="http://www.w3.org/2000/svg"><title>Turborepo</title><defs><linearGradient gradientUnits="userSpaceOnUse" id="logo-ring-gradient" x1="15.0234" x2="3.64419" y1="4.00556" y2="15.3847"><stop stop-color="#0096FF"></stop><stop offset="1" stop-color="#FF1E56"></stop></linearGradient><linearGradient id="gradient"><stop offset="0%" stop-color="#000000"></stop><stop offset="25%" stop-color="#ffffff"></stop><stop offset="85%" stop-color="#ffffff"></stop><stop offset="100%" stop-color="#000000"></stop></linearGradient><mask id="logo-mask"><rect fill="url(#gradient)" height="26" transform="translate(-8,0)" width="46" x="0" y="0"></rect></mask></defs><g mask="url(#logo-mask)" transform="translate(8,0)"><g class="relative z-0" opacity="1" style="transform: none; transform-origin: 13.9488px 13.9398px 0px;" transform-origin="13.948790550231934px 13.939799308776855px"><path class="fill-black dark:fill-white" d="M13.9396 6.42181C9.79423 6.42181 6.42163 9.79441 6.42163 13.9398C6.42163 18.0852 9.79423 21.4578 13.9396 21.4578C18.085 21.4578 21.4576 18.0852 21.4576 13.9398C21.4576 9.79441 18.085 6.42181 13.9396 6.42181ZM13.9396 17.8304C11.7906 17.8304 10.049 16.0888 10.049 13.9398C10.049 11.7908 11.7906 10.0492 13.9396 10.0492C16.0886 10.0492 17.8302 11.7908 17.8302 13.9398C17.8302 16.0888 16.0886 17.8304 13.9396 17.8304Z"></path><path clip-rule="evenodd" d="M14.5697 5.187V2.38C20.6709 2.7062 25.5177 7.7574 25.5177 13.9398C25.5177 20.1222 20.6709 25.172 14.5697 25.4996V22.6926C19.1169 22.3678 22.7177 18.5682 22.7177 13.9398C22.7177 9.3114 19.1169 5.5118 14.5697 5.187ZM7.30928 19.6798C6.10388 18.2882 5.32688 16.5158 5.18828 14.5698H2.37988C2.52548 17.2928 3.61468 19.7638 5.32128 21.6664L7.30788 19.6798H7.30928ZM13.3097 25.4996V22.6926C11.3623 22.554 9.5899 21.7784 8.1983 20.5716L6.2117 22.5582C8.1157 24.2662 10.5867 25.354 13.3083 25.4996H13.3097Z" fill="url(#logo-ring-gradient)" fill-rule="evenodd"></path></g></g><g class="relative z-10 header-logo_desktopLogo__zIjld" transform="translate(8,0)"><path class="fill-black dark:fill-white" d="M48.2623 11.2944V8.24418H33.5623V11.2944H39.1115V21.4374H42.713V11.2944H48.2623Z"></path><path class="fill-black dark:fill-white" d="M56.5679 21.6396C61.0882 21.6396 63.5688 19.3427 63.5688 15.5574V8.24418H59.9673V15.2083C59.9673 17.3214 58.8648 18.5158 56.5679 18.5158C54.271 18.5158 53.1685 17.3214 53.1685 15.2083V8.24418H49.567V15.5574C49.567 19.3427 52.0476 21.6396 56.5679 21.6396Z"></path><path class="fill-black dark:fill-white" d="M69.0819 17.0642H72.665L75.4947 21.4374H79.6291L76.4319 16.6783C78.2326 16.0352 79.3351 14.6019 79.3351 12.6542C79.3351 9.82443 77.222 8.24418 74.0064 8.24418H65.4804V21.4374H69.0819V17.0642ZM69.0819 14.2161V11.2577H73.8226C75.0905 11.2577 75.7887 11.8089 75.7887 12.7461C75.7887 13.6281 75.0905 14.2161 73.8226 14.2161H69.0819Z"></path><path class="fill-black dark:fill-white" d="M81.0108 21.4374H90.4372C93.3772 21.4374 95.0677 20.0409 95.0677 17.7073C95.0677 16.1454 94.0754 15.0797 92.8994 14.6019C93.7079 14.2161 94.7002 13.2973 94.7002 11.8457C94.7002 9.51206 93.0464 8.24418 90.1248 8.24418H81.0108V21.4374ZM84.4653 13.4076V11.1658H89.7573C90.7496 11.1658 91.3008 11.5517 91.3008 12.2867C91.3008 13.0217 90.7496 13.4076 89.7573 13.4076H84.4653ZM84.4653 16.1087H90.0881C91.0619 16.1087 91.5948 16.5864 91.5948 17.3031C91.5948 18.0197 91.0619 18.4974 90.0881 18.4974H84.4653V16.1087Z"></path><path class="fill-black dark:fill-white" d="M103.873 8.02368C99.2612 8.02368 95.9353 10.9086 95.9353 14.8408C95.9353 18.7731 99.2612 21.6579 103.873 21.6579C108.485 21.6579 111.793 18.7731 111.793 14.8408C111.793 10.9086 108.485 8.02368 103.873 8.02368ZM103.873 11.1474C106.299 11.1474 108.118 12.5807 108.118 14.8408C108.118 17.1009 106.299 18.5342 103.873 18.5342C101.448 18.5342 99.6287 17.1009 99.6287 14.8408C99.6287 12.5807 101.448 11.1474 103.873 11.1474Z"></path></g></svg>

---
title: Announcement
---

<div class="text-black dark:text-white text-7xl font-bold leading-relaxed">

- React 19
- Next.js 15
- nuqs 2

</div>

---
title: v2 Features
---

<div class="text-black dark:text-white text-5xl font-semibold leading-relaxed">

- Smaller bundle size
- ESM only
- No more patching internals <span class="text-zinc-500">(maybe)</span>
- Fewer hacks

</div>

---
title: Thank you!
---

<h1 class="text-8xl text-center">Thank you!</h1>

<div class="grid grid-cols-2 gap-x-48">
  <div class="flex justify-center mt-10">
    <div class="p-4 bg-white inline-block">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 29 29" class="size-48"><path fill="#ffffff" d="M0,0 h29v29H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM9 0h1v1H9zM12 0h3v1H12zM16 0h2v1H16zM19 0h1v1H19zM22,0 h7v1H22zM0 1h1v1H0zM6 1h1v1H6zM8 1h3v1H8zM13 1h1v1H13zM18 1h1v1H18zM20 1h1v1H20zM22 1h1v1H22zM28,1 h1v1H28zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM8 2h3v1H8zM13 2h2v1H13zM22 2h1v1H22zM24 2h3v1H24zM28,2 h1v1H28zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM9 3h2v1H9zM14 3h2v1H14zM17 3h2v1H17zM22 3h1v1H22zM24 3h3v1H24zM28,3 h1v1H28zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM9 4h4v1H9zM15 4h1v1H15zM18 4h3v1H18zM22 4h1v1H22zM24 4h3v1H24zM28,4 h1v1H28zM0 5h1v1H0zM6 5h1v1H6zM10 5h1v1H10zM15 5h1v1H15zM18 5h3v1H18zM22 5h1v1H22zM28,5 h1v1H28zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22,6 h7v1H22zM9 7h2v1H9zM12 7h1v1H12zM17 7h3v1H17zM1 8h3v1H1zM5 8h2v1H5zM14 8h4v1H14zM20 8h1v1H20zM26 8h2v1H26zM0 9h1v1H0zM3 9h1v1H3zM5 9h1v1H5zM7 9h3v1H7zM14 9h3v1H14zM19 9h2v1H19zM22 9h5v1H22zM28,9 h1v1H28zM3 10h1v1H3zM5 10h5v1H5zM22 10h1v1H22zM25 10h1v1H25zM27 10h1v1H27zM0 11h1v1H0zM8 11h1v1H8zM19 11h1v1H19zM23 11h1v1H23zM28,11 h1v1H28zM1 12h6v1H1zM9 12h1v1H9zM21 12h1v1H21zM23 12h1v1H23zM26,12 h3v1H26zM0 13h1v1H0zM2 13h3v1H2zM7 13h1v1H7zM19 13h1v1H19zM22 13h2v1H22zM25 13h2v1H25zM28,13 h1v1H28zM3 14h1v1H3zM6 14h4v1H6zM19 14h2v1H19zM22 14h4v1H22zM27,14 h2v1H27zM1 15h3v1H1zM5 15h1v1H5zM9 15h1v1H9zM19 15h2v1H19zM24 15h2v1H24zM28,15 h1v1H28zM0 16h2v1H0zM5 16h3v1H5zM21 16h1v1H21zM24 16h2v1H24zM1 17h2v1H1zM4 17h2v1H4zM7 17h1v1H7zM9 17h1v1H9zM20 17h2v1H20zM23 17h1v1H23zM26 17h1v1H26zM0 18h1v1H0zM2 18h2v1H2zM6 18h1v1H6zM8 18h2v1H8zM20 18h1v1H20zM22 18h1v1H22zM25 18h1v1H25zM4 19h2v1H4zM7 19h4v1H7zM12 19h2v1H12zM15 19h5v1H15zM21 19h2v1H21zM24 19h1v1H24zM26 19h2v1H26zM1 20h1v1H1zM3 20h2v1H3zM6 20h2v1H6zM11 20h1v1H11zM14 20h5v1H14zM20 20h8v1H20zM8 21h3v1H8zM17 21h2v1H17zM20 21h1v1H20zM24 21h2v1H24zM27,21 h2v1H27zM0 22h7v1H0zM9 22h2v1H9zM12 22h1v1H12zM16 22h1v1H16zM18 22h3v1H18zM22 22h1v1H22zM24 22h1v1H24zM26 22h2v1H26zM0 23h1v1H0zM6 23h1v1H6zM8 23h2v1H8zM11 23h1v1H11zM15 23h1v1H15zM17 23h1v1H17zM20 23h1v1H20zM24 23h1v1H24zM0 24h1v1H0zM2 24h3v1H2zM6 24h1v1H6zM9 24h1v1H9zM11 24h6v1H11zM20 24h7v1H20zM28,24 h1v1H28zM0 25h1v1H0zM2 25h3v1H2zM6 25h1v1H6zM8 25h1v1H8zM10 25h1v1H10zM13 25h1v1H13zM19 25h1v1H19zM24 25h2v1H24zM27 25h1v1H27zM0 26h1v1H0zM2 26h3v1H2zM6 26h1v1H6zM8 26h3v1H8zM12 26h2v1H12zM17 26h2v1H17zM20 26h1v1H20zM23 26h1v1H23zM26 26h1v1H26zM28,26 h1v1H28zM0 27h1v1H0zM6 27h1v1H6zM8 27h1v1H8zM10 27h1v1H10zM13 27h3v1H13zM18 27h4v1H18zM24 27h2v1H24zM27 27h1v1H27zM0 28h7v1H0zM11 28h2v1H11zM18 28h1v1H18zM20 28h4v1H20zM27 28h1v1H27z" shapeRendering="crispEdges"></path><image href="/img/nuqs-light.svg" height="9" width="9" x="10" y="10" preserveAspectRatio="none"></image></svg>
    </div>
  </div>
  <div>
    <div class="flex justify-center mt-10">
      <div class="p-4 bg-white inline-block">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 33 33" class="size-48"><path fill="#ffffff" d="M0,0 h33v33H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM12 0h2v1H12zM16 0h3v1H16zM21 0h1v1H21zM23 0h1v1H23zM26,0 h7v1H26zM0 1h1v1H0zM6 1h1v1H6zM9 1h1v1H9zM12 1h2v1H12zM15 1h1v1H15zM17 1h1v1H17zM19 1h2v1H19zM22 1h1v1H22zM26 1h1v1H26zM32,1 h1v1H32zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM8 2h1v1H8zM11 2h2v1H11zM14 2h2v1H14zM20 2h2v1H20zM24 2h1v1H24zM26 2h1v1H26zM28 2h3v1H28zM32,2 h1v1H32zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM10 3h4v1H10zM15 3h1v1H15zM17 3h2v1H17zM20 3h1v1H20zM22 3h3v1H22zM26 3h1v1H26zM28 3h3v1H28zM32,3 h1v1H32zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM8 4h2v1H8zM13 4h2v1H13zM16 4h1v1H16zM18 4h7v1H18zM26 4h1v1H26zM28 4h3v1H28zM32,4 h1v1H32zM0 5h1v1H0zM6 5h1v1H6zM8 5h1v1H8zM10 5h1v1H10zM12 5h1v1H12zM14 5h3v1H14zM18 5h2v1H18zM21 5h2v1H21zM24 5h1v1H24zM26 5h1v1H26zM32,5 h1v1H32zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22 6h1v1H22zM24 6h1v1H24zM26,6 h7v1H26zM12 7h2v1H12zM17 7h2v1H17zM21 7h2v1H21zM1 8h1v1H1zM4 8h1v1H4zM6 8h1v1H6zM8 8h3v1H8zM12 8h6v1H12zM19 8h1v1H19zM21 8h2v1H21zM25 8h1v1H25zM27 8h2v1H27zM30 8h1v1H30zM0 9h2v1H0zM4 9h2v1H4zM8 9h2v1H8zM12 9h2v1H12zM18 9h1v1H18zM23 9h3v1H23zM29 9h3v1H29zM0 10h1v1H0zM2 10h2v1H2zM5 10h3v1H5zM9 10h4v1H9zM15 10h1v1H15zM17 10h1v1H17zM20 10h4v1H20zM29 10h1v1H29zM31 10h1v1H31zM3 11h2v1H3zM9 11h1v1H9zM11 11h2v1H11zM14 11h1v1H14zM16 11h6v1H16zM23 11h3v1H23zM31 11h1v1H31zM0 12h3v1H0zM6 12h1v1H6zM26 12h1v1H26zM28 12h2v1H28zM0 13h2v1H0zM3 13h2v1H3zM8 13h2v1H8zM23 13h1v1H23zM25 13h1v1H25zM27 13h1v1H27zM29 13h2v1H29zM2 14h1v1H2zM4 14h1v1H4zM6 14h4v1H6zM11 14h1v1H11zM23 14h5v1H23zM29 14h3v1H29zM2 15h3v1H2zM10 15h1v1H10zM21 15h1v1H21zM23 15h1v1H23zM25 15h4v1H25zM2 16h5v1H2zM8 16h2v1H8zM11 16h1v1H11zM21 16h1v1H21zM26 16h1v1H26zM28 16h1v1H28zM31 16h1v1H31zM7 17h1v1H7zM9 17h3v1H9zM21 17h1v1H21zM23 17h3v1H23zM29 17h3v1H29zM0 18h5v1H0zM6 18h2v1H6zM9 18h3v1H9zM23 18h1v1H23zM27 18h1v1H27zM29 18h1v1H29zM2 19h4v1H2zM8 19h1v1H8zM10 19h2v1H10zM22 19h1v1H22zM24 19h4v1H24zM31,19 h2v1H31zM0 20h1v1H0zM2 20h1v1H2zM6 20h3v1H6zM10 20h1v1H10zM22 20h2v1H22zM26 20h1v1H26zM28 20h2v1H28zM31 20h1v1H31zM0 21h1v1H0zM2 21h2v1H2zM13 21h4v1H13zM18 21h4v1H18zM23 21h1v1H23zM25 21h1v1H25zM27 21h1v1H27zM29 21h3v1H29zM3 22h1v1H3zM6 22h1v1H6zM8 22h3v1H8zM12 22h2v1H12zM16 22h1v1H16zM20 22h1v1H20zM23 22h3v1H23zM27 22h2v1H27zM31 22h1v1H31zM3 23h3v1H3zM7 23h1v1H7zM10 23h3v1H10zM15 23h3v1H15zM21 23h2v1H21zM24 23h3v1H24zM28 23h1v1H28zM32,23 h1v1H32zM0 24h9v1H0zM10 24h2v1H10zM14 24h1v1H14zM16 24h13v1H16zM32,24 h1v1H32zM8 25h2v1H8zM11 25h2v1H11zM16 25h2v1H16zM24 25h1v1H24zM28 25h1v1H28zM30 25h2v1H30zM0 26h7v1H0zM10 26h1v1H10zM13 26h3v1H13zM20 26h3v1H20zM24 26h1v1H24zM26 26h1v1H26zM28 26h2v1H28zM31 26h1v1H31zM0 27h1v1H0zM6 27h1v1H6zM9 27h1v1H9zM13 27h1v1H13zM15 27h7v1H15zM23 27h2v1H23zM28 27h1v1H28zM0 28h1v1H0zM2 28h3v1H2zM6 28h1v1H6zM8 28h3v1H8zM12 28h1v1H12zM14 28h2v1H14zM20 28h1v1H20zM24 28h6v1H24zM0 29h1v1H0zM2 29h3v1H2zM6 29h1v1H6zM10 29h3v1H10zM16 29h1v1H16zM18 29h2v1H18zM22 29h2v1H22zM26 29h6v1H26zM0 30h1v1H0zM2 30h3v1H2zM6 30h1v1H6zM9 30h1v1H9zM11 30h6v1H11zM18 30h2v1H18zM22 30h1v1H22zM24 30h1v1H24zM26 30h3v1H26zM0 31h1v1H0zM6 31h1v1H6zM8 31h3v1H8zM15 31h3v1H15zM19 31h3v1H19zM24 31h1v1H24zM26 31h1v1H26zM0 32h7v1H0zM10 32h2v1H10zM13 32h1v1H13zM17 32h1v1H17zM20 32h3v1H20zM24 32h1v1H24zM32,32 h1v1H32z" shapeRendering="crispEdges"></path><image href="/img/forkit-icon.png" height="7" width="7" x="13" y="13" ></image></svg>
      </div>
    </div>
  </div>
  <p class="text-center text-3xl font-semibold">nuqs.47ng.com</p>
  <p class="text-center text-3xl font-semibold">OpenFeedback</p>
</div>
