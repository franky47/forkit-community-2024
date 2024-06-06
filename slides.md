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

Feedback & tips

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
Before we start: light mode or dark mode?

Thanks to the sponsors & Bear Studio

This is my first talk at a tech conference,<br/>
so please bear with me.
-->

---
title: What to expect
---

<h1 class="text-8xl text-center">What to expect</h1>

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
    <div class="text-5xl text-zinc-500">
      @fortysevenfx
    </div>
  </div>
</div>

<div class="flex justify-center mt-10">
  <div class="p-4 bg-white inline-block">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 29 29" class="w-48 h-48">
      <path fill="#ffffff" d="M0,0 h29v29H0z" shapeRendering="crispEdges"/>
      <path fill="#000000" d="M0 0h7v1H0zM9 0h1v1H9zM11 0h2v1H11zM14 0h4v1H14zM20 0h1v1H20zM22,0 h7v1H22zM0 1h1v1H0zM6 1h1v1H6zM8 1h1v1H8zM10 1h2v1H10zM17 1h4v1H17zM22 1h1v1H22zM28,1 h1v1H28zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM11 2h1v1H11zM13 2h1v1H13zM15 2h2v1H15zM18 2h2v1H18zM22 2h1v1H22zM24 2h3v1H24zM28,2 h1v1H28zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM8 3h2v1H8zM12 3h4v1H12zM17 3h4v1H17zM22 3h1v1H22zM24 3h3v1H24zM28,3 h1v1H28zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM8 4h1v1H8zM10 4h2v1H10zM14 4h2v1H14zM18 4h2v1H18zM22 4h1v1H22zM24 4h3v1H24zM28,4 h1v1H28zM0 5h1v1H0zM6 5h1v1H6zM9 5h3v1H9zM13 5h4v1H13zM20 5h1v1H20zM22 5h1v1H22zM28,5 h1v1H28zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22,6 h7v1H22zM8 7h1v1H8zM19 7h1v1H19zM1 8h1v1H1zM3 8h4v1H3zM8 8h3v1H8zM12 8h1v1H12zM16 8h2v1H16zM19 8h4v1H19zM24 8h2v1H24zM27 8h1v1H27zM0 9h1v1H0zM2 9h3v1H2zM7 9h1v1H7zM9 9h3v1H9zM13 9h2v1H13zM17 9h1v1H17zM19 9h1v1H19zM21 9h1v1H21zM23 9h2v1H23zM26 9h2v1H26zM0 10h1v1H0zM3 10h1v1H3zM5 10h2v1H5zM9 10h1v1H9zM20 10h3v1H20zM24 10h1v1H24zM0 11h1v1H0zM2 11h2v1H2zM5 11h1v1H5zM9 11h1v1H9zM19 11h2v1H19zM24 11h2v1H24zM28,11 h1v1H28zM2 12h2v1H2zM5 12h4v1H5zM19 12h1v1H19zM21 12h2v1H21zM27 12h1v1H27zM7 13h1v1H7zM22 13h1v1H22zM24 13h1v1H24zM26,13 h3v1H26zM0 14h2v1H0zM6 14h2v1H6zM19 14h1v1H19zM22 14h2v1H22zM25 14h1v1H25zM28,14 h1v1H28zM2 15h4v1H2zM7 15h2v1H7zM24 15h4v1H24zM0 16h1v1H0zM2 16h6v1H2zM20 16h1v1H20zM23 16h1v1H23zM25 16h1v1H25zM28,16 h1v1H28zM0 17h2v1H0zM4 17h1v1H4zM8 17h2v1H8zM19 17h2v1H19zM24 17h2v1H24zM0 18h2v1H0zM4 18h1v1H4zM6 18h2v1H6zM9 18h1v1H9zM19 18h2v1H19zM25 18h2v1H25zM28,18 h1v1H28zM0 19h2v1H0zM4 19h2v1H4zM7 19h4v1H7zM13 19h2v1H13zM21 19h2v1H21zM24 19h1v1H24zM26 19h1v1H26zM0 20h7v1H0zM8 20h5v1H8zM15 20h3v1H15zM20 20h5v1H20zM26,20 h3v1H26zM8 21h1v1H8zM12 21h2v1H12zM15 21h1v1H15zM18 21h1v1H18zM20 21h1v1H20zM24 21h3v1H24zM0 22h7v1H0zM9 22h3v1H9zM15 22h2v1H15zM18 22h3v1H18zM22 22h1v1H22zM24 22h1v1H24zM26 22h1v1H26zM0 23h1v1H0zM6 23h1v1H6zM8 23h2v1H8zM11 23h1v1H11zM15 23h1v1H15zM17 23h4v1H17zM24 23h2v1H24zM0 24h1v1H0zM2 24h3v1H2zM6 24h1v1H6zM8 24h1v1H8zM10 24h1v1H10zM13 24h1v1H13zM18 24h7v1H18zM28,24 h1v1H28zM0 25h1v1H0zM2 25h3v1H2zM6 25h1v1H6zM8 25h4v1H8zM15 25h1v1H15zM17 25h1v1H17zM23 25h1v1H23zM25 25h1v1H25zM28,25 h1v1H28zM0 26h1v1H0zM2 26h3v1H2zM6 26h1v1H6zM12 26h1v1H12zM14 26h2v1H14zM18 26h1v1H18zM20 26h2v1H20zM23 26h2v1H23zM27,26 h2v1H27zM0 27h1v1H0zM6 27h1v1H6zM8 27h2v1H8zM11 27h1v1H11zM14 27h1v1H14zM18 27h1v1H18zM21 27h2v1H21zM24 27h3v1H24zM28,27 h1v1H28zM0 28h7v1H0zM9 28h2v1H9zM13 28h2v1H13zM18 28h3v1H18zM23 28h3v1H23z" shapeRendering="crispEdges"/>
      <image href="/img/x.svg" height="7.25" width="7.25" x="10.875" y="10.875" preserveAspectRatio="none"/>
    </svg>
  </div>
</div>

<!--
My name is François Best, you can find me on Twitter as @fortysevenfx.
-->

---
title: What I do
---

<p class="text-center text-black dark:text-white text-5xl font-semibold">Freelance web developer @ 47ng</p>

<div class="grid grid-cols-5 items-center justify-center gap-x-12 gap-y-4 text-center text-3xl text-zinc-500  mt-20">
  <img src="/img/react.svg" alt="React" class="w-32 h-32" />
  <img src="/img/next.svg" alt="Next.js" class="w-32 h-32" />
  <img src="/img/typescript.svg" alt="Fastify" class="w-32 h-32" />
  <img src="/img/fastify-dark.svg" alt="Fastify" class="w-32 h-32 hidden dark:block" />
  <img src="/img/fastify-light.svg" alt="Fastify" class="w-32 h-32 block dark:hidden" />
  <img src="/img/nodejs.svg" alt="Node.js" class="w-32 h-32" />
  <label>React</label>
  <label>Next.js</label>
  <label>TypeScript</label>
  <label>Fastify</label>
  <label>Node.js</label>
</div>

<!--
I'm a freelance web developer since 2018.
Mostly front-end with React & Next.js
Sometimes full-stack with Node.js & Fastify
 -->

---
title: Before that (studio)
layout: image
image: /img/ssl.jpg
backgroundSize: fit
---

<!-- Before that, I used to work in the audio industry where we turned analog recording studio gear like this...
-->

---
title: Before that (VMR)
layout: image
image: /img/vmr.jpg
backgroundSize: 120vh
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

<!-- I started using web technologies 8 years ago,
<br/>
when these started to become popular.
-->

---
title: Beauty of the web
---

<div class="text-black dark:text-white text-7xl font-medium leading-relaxed">

- <span class="text-zinc-500">1.</span> `git push`
- <span class="text-zinc-500">2.</span> Visit the website
- <span class="text-zinc-500">3.</span> 😍

</div>

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

---
title: What we can do with URLs
---

<div class="text-black dark:text-white text-7xl font-medium leading-relaxed">

- Share them
- Bookmark them
- Navigate history

</div>

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

---
title: Routing in frameworks
---

<p class="text-4xl text-black dark:text-white">In Next.js</p>

<pre class="text-3xl">
src/app/pathname/page.tsx -> /pathname
</pre>

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

<!-- todo: Add an example with GitHub issues comments -->

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

---
title: Woodworking
layout: image
image: /img/mallet.jpeg
backgroundSize: contain
class: bg-white
---

---
title: Dovetail designer
layout: image
image: /img/dovetail-light.png
backgroundSize: contain
class: bg-white
---


---
title: Query string in Next.js
---

<p class="text-5xl font-bold text-black dark:text-white text-center">In Next.js</p>

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


---
title: next-usequerystate
---

<h1 class="text-6xl font-bold text-black dark:text-white text-center mb-12">next-usequerystate</h1>

```tsx
import { useQueryState } from 'next-usequerystate'

function SearchComponent() {
  const [search, setSearch] = useQueryState('search', {
    defaultValue: ''
  })
  return (
    <input
      type="search"
      value={search}
      onChange={e => setSearch(e.target.value)}
    />
  )
}
```

<style>
pre {
  font-size: 1.5rem;
}
</style>

<!-- That was in 2020 -->


---
title: Users
---

<h1 class="text-6xl text-center mb-12 -mt-8">Used by</h1>

<svg aria-label="Vercel" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 284 65" class="fill-black dark:fill-white mx-auto h-20 mb-6">
  <path d="M141.68 16.25c-11.04 0-19 7.2-19 18s8.96 18 20 18c6.67 0 12.55-2.64 16.19-7.09l-7.65-4.42c-2.02 2.21-5.09 3.5-8.54 3.5-4.79 0-8.86-2.5-10.37-6.5h28.02c.22-1.12.35-2.28.35-3.5 0-10.79-7.96-17.99-19-17.99zm-9.46 14.5c1.25-3.99 4.67-6.5 9.45-6.5 4.79 0 8.21 2.51 9.45 6.5h-18.9zm117.14-14.5c-11.04 0-19 7.2-19 18s8.96 18 20 18c6.67 0 12.55-2.64 16.19-7.09l-7.65-4.42c-2.02 2.21-5.09 3.5-8.54 3.5-4.79 0-8.86-2.5-10.37-6.5h28.02c.22-1.12.35-2.28.35-3.5 0-10.79-7.96-17.99-19-17.99zm-9.45 14.5c1.25-3.99 4.67-6.5 9.45-6.5 4.79 0 8.21 2.51 9.45 6.5h-18.9zm-39.03 3.5c0 6 3.92 10 10 10 4.12 0 7.21-1.87 8.8-4.92l7.68 4.43c-3.18 5.3-9.14 8.49-16.48 8.49-11.05 0-19-7.2-19-18s7.96-18 19-18c7.34 0 13.29 3.19 16.48 8.49l-7.68 4.43c-1.59-3.05-4.68-4.92-8.8-4.92-6.07 0-10 4-10 10zm82.48-29v46h-9v-46h9zM37.59.25l36.95 64H.64l36.95-64zm92.38 5l-27.71 48-27.71-48h10.39l17.32 30 17.32-30h10.39zm58.91 12v9.69c-1-.29-2.06-.49-3.2-.49-5.81 0-10 4-10 10v14.8h-9v-34h9v9.2c0-5.08 5.91-9.2 13.2-9.2z"
  />
</svg>

<div style="width: 90%;" class="bg-red-500 mx-auto">
<img src="/img/users-light.png" alt="Users" class="block dark:hidden"/>
<img src="/img/users-dark.png" alt="Users" class="hidden dark:block"/>
</div>

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


---
title: Star history
layout: image
image: /img/star-history.png
backgroundSize: contain
class: bg-white
---

---
title: RSC
---

<h1 class="text-6xl text-center">React Server Components</h1>

---
title: Server-first
---

<h1 class="text-9xl text-center">Server-first</h1>

---
title: Shallow routing
---

<h1 class="text-8xl text-center">Shallow routing</h1>

---
title: Shallow in nuqs
---


```tsx
useQueryState('client', { shallow: true })
useQueryState('server', { shallow: false })
```

<style>
pre, code {
  font-size: 1.5rem;
}
</style>

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

<style>
pre, code {
  font-size: 2rem;
}
</style>

---
title: Rate limits
---

<h1 class="text-9xl text-center">Rate limits</h1>

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
layout: image
image: /img/sub-release.png
backgroundSize: contain
class: bg-black
---

---
title: Too many releases
layout: image
image: /img/next-releases.png
backgroundSize: contain
class: bg-black
---

---
title: What are our options?
---

<h1 class="text-8xl text-center leading-tight">What are<br/>our options?</h1>

---
title: GitHub API
---

<h1 class="text-9xl text-center">GitHub API</h1>

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

---
title: App router Redux
---

<h1 class="text-center flex items-center gap-24">
  <img src="/img/next.svg" class="h-48 block"/>
  <span class="text-8xl">❤️</span>
  <img src="/img/redux.svg" class="h-48 block"/>
</h1>

---
title: Test matrix
layout: image-left
image: /img/matrix.png
---

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
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 29 29" class="size-48"><path fill="#ffffff" d="M0,0 h29v29H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM9 0h3v1H9zM13 0h1v1H13zM15 0h1v1H15zM19 0h1v1H19zM22,0 h7v1H22zM0 1h1v1H0zM6 1h1v1H6zM10 1h1v1H10zM12 1h1v1H12zM14 1h3v1H14zM22 1h1v1H22zM28,1 h1v1H28zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM9 2h1v1H9zM14 2h1v1H14zM16 2h1v1H16zM19 2h2v1H19zM22 2h1v1H22zM24 2h3v1H24zM28,2 h1v1H28zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM9 3h2v1H9zM13 3h1v1H13zM15 3h5v1H15zM22 3h1v1H22zM24 3h3v1H24zM28,3 h1v1H28zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM8 4h2v1H8zM13 4h1v1H13zM15 4h3v1H15zM19 4h1v1H19zM22 4h1v1H22zM24 4h3v1H24zM28,4 h1v1H28zM0 5h1v1H0zM6 5h1v1H6zM11 5h1v1H11zM16 5h1v1H16zM19 5h2v1H19zM22 5h1v1H22zM28,5 h1v1H28zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22,6 h7v1H22zM8 7h3v1H8zM13 7h1v1H13zM16 7h3v1H16zM2 8h2v1H2zM6 8h3v1H6zM10 8h4v1H10zM19 8h4v1H19zM24 8h1v1H24zM0 9h2v1H0zM3 9h1v1H3zM11 9h1v1H11zM17 9h3v1H17zM22 9h3v1H22zM26 9h1v1H26zM28,9 h1v1H28zM1 10h4v1H1zM6 10h2v1H6zM9 10h1v1H9zM20 10h1v1H20zM22 10h1v1H22zM26 10h2v1H26zM0 11h1v1H0zM2 11h2v1H2zM5 11h1v1H5zM7 11h1v1H7zM25 11h1v1H25zM28,11 h1v1H28zM0 12h1v1H0zM2 12h2v1H2zM5 12h3v1H5zM9 12h1v1H9zM20 12h2v1H20zM23 12h1v1H23zM26,12 h3v1H26zM1 13h1v1H1zM19 13h1v1H19zM22 13h2v1H22zM25 13h2v1H25zM28,13 h1v1H28zM2 14h7v1H2zM19 14h1v1H19zM22 14h4v1H22zM27,14 h2v1H27zM2 15h1v1H2zM4 15h2v1H4zM7 15h1v1H7zM20 15h1v1H20zM22 15h1v1H22zM24 15h2v1H24zM28,15 h1v1H28zM0 16h1v1H0zM2 16h1v1H2zM5 16h2v1H5zM8 16h1v1H8zM24 16h2v1H24zM1 17h5v1H1zM7 17h1v1H7zM20 17h2v1H20zM23 17h1v1H23zM26 17h1v1H26zM0 18h1v1H0zM3 18h2v1H3zM6 18h2v1H6zM9 18h1v1H9zM20 18h1v1H20zM22 18h5v1H22zM4 19h2v1H4zM7 19h2v1H7zM10 19h1v1H10zM12 19h1v1H12zM15 19h2v1H15zM18 19h1v1H18zM20 19h3v1H20zM25 19h2v1H25zM1 20h2v1H1zM6 20h1v1H6zM8 20h3v1H8zM12 20h1v1H12zM14 20h1v1H14zM16 20h1v1H16zM18 20h9v1H18zM8 21h2v1H8zM11 21h1v1H11zM15 21h1v1H15zM20 21h1v1H20zM24 21h2v1H24zM28,21 h1v1H28zM0 22h7v1H0zM8 22h5v1H8zM15 22h2v1H15zM18 22h3v1H18zM22 22h1v1H22zM24 22h1v1H24zM26 22h2v1H26zM0 23h1v1H0zM6 23h1v1H6zM10 23h2v1H10zM13 23h2v1H13zM16 23h1v1H16zM20 23h1v1H20zM24 23h1v1H24zM0 24h1v1H0zM2 24h3v1H2zM6 24h1v1H6zM9 24h1v1H9zM11 24h1v1H11zM14 24h3v1H14zM18 24h1v1H18zM20 24h7v1H20zM28,24 h1v1H28zM0 25h1v1H0zM2 25h3v1H2zM6 25h1v1H6zM8 25h3v1H8zM14 25h2v1H14zM19 25h1v1H19zM24 25h2v1H24zM27 25h1v1H27zM0 26h1v1H0zM2 26h3v1H2zM6 26h1v1H6zM8 26h1v1H8zM10 26h1v1H10zM12 26h1v1H12zM20 26h1v1H20zM23 26h1v1H23zM25 26h2v1H25zM28,26 h1v1H28zM0 27h1v1H0zM6 27h1v1H6zM9 27h1v1H9zM11 27h6v1H11zM18 27h3v1H18zM22 27h1v1H22zM24 27h2v1H24zM27 27h1v1H27zM0 28h7v1H0zM9 28h2v1H9zM12 28h12v1H12zM25 28h1v1H25zM27 28h1v1H27z" shapeRendering="crispEdges"></path><image href="/img/nuqs-light.svg" height="9" width="9" x="10" y="10" preserveAspectRatio="none"></image></svg>
    </div>
  </div>
  <div>
    <div class="flex justify-center mt-10">
      <div class="p-4 bg-white inline-block">
        <svg xmlns="http://www.w3.org/2000/svg" class="size-48" viewBox="0 0 33 33"><path fill="#ffffff" d="M0,0 h33v33H0z" shapeRendering="crispEdges"></path><path fill="#000000" d="M0 0h7v1H0zM8 0h3v1H8zM12 0h1v1H12zM14 0h1v1H14zM18 0h2v1H18zM23 0h2v1H23zM26,0 h7v1H26zM0 1h1v1H0zM6 1h1v1H6zM8 1h1v1H8zM10 1h2v1H10zM15 1h3v1H15zM19 1h1v1H19zM22 1h1v1H22zM24 1h1v1H24zM26 1h1v1H26zM32,1 h1v1H32zM0 2h1v1H0zM2 2h3v1H2zM6 2h1v1H6zM8 2h1v1H8zM12 2h2v1H12zM17 2h2v1H17zM20 2h5v1H20zM26 2h1v1H26zM28 2h3v1H28zM32,2 h1v1H32zM0 3h1v1H0zM2 3h3v1H2zM6 3h1v1H6zM9 3h1v1H9zM12 3h1v1H12zM16 3h5v1H16zM22 3h2v1H22zM26 3h1v1H26zM28 3h3v1H28zM32,3 h1v1H32zM0 4h1v1H0zM2 4h3v1H2zM6 4h1v1H6zM9 4h3v1H9zM13 4h2v1H13zM21 4h4v1H21zM26 4h1v1H26zM28 4h3v1H28zM32,4 h1v1H32zM0 5h1v1H0zM6 5h1v1H6zM8 5h1v1H8zM14 5h3v1H14zM19 5h1v1H19zM21 5h2v1H21zM26 5h1v1H26zM32,5 h1v1H32zM0 6h7v1H0zM8 6h1v1H8zM10 6h1v1H10zM12 6h1v1H12zM14 6h1v1H14zM16 6h1v1H16zM18 6h1v1H18zM20 6h1v1H20zM22 6h1v1H22zM24 6h1v1H24zM26,6 h7v1H26zM8 7h5v1H8zM16 7h2v1H16zM19 7h1v1H19zM21 7h1v1H21zM2 8h3v1H2zM6 8h1v1H6zM8 8h1v1H8zM10 8h1v1H10zM12 8h1v1H12zM14 8h1v1H14zM16 8h1v1H16zM18 8h2v1H18zM22 8h6v1H22zM30,8 h3v1H30zM0 9h2v1H0zM3 9h1v1H3zM7 9h3v1H7zM12 9h1v1H12zM14 9h1v1H14zM20 9h2v1H20zM23 9h1v1H23zM25 9h2v1H25zM29 9h1v1H29zM31,9 h2v1H31zM0 10h4v1H0zM6 10h1v1H6zM11 10h2v1H11zM16 10h1v1H16zM18 10h1v1H18zM21 10h1v1H21zM25 10h3v1H25zM30 10h2v1H30zM1 11h1v1H1zM5 11h1v1H5zM7 11h1v1H7zM9 11h1v1H9zM11 11h3v1H11zM16 11h3v1H16zM21 11h2v1H21zM26 11h1v1H26zM29 11h2v1H29zM1 12h2v1H1zM4 12h1v1H4zM6 12h1v1H6zM8 12h4v1H8zM21 12h1v1H21zM24 12h2v1H24zM28 12h1v1H28zM31 12h1v1H31zM0 13h1v1H0zM3 13h1v1H3zM8 13h2v1H8zM11 13h1v1H11zM23 13h4v1H23zM30 13h1v1H30zM32,13 h1v1H32zM0 14h4v1H0zM6 14h1v1H6zM8 14h2v1H8zM11 14h1v1H11zM22 14h1v1H22zM24 14h2v1H24zM28 14h2v1H28zM31 14h1v1H31zM0 15h4v1H0zM8 15h3v1H8zM21 15h2v1H21zM24 15h1v1H24zM26 15h1v1H26zM28 15h4v1H28zM0 16h2v1H0zM6 16h2v1H6zM10 16h1v1H10zM23 16h1v1H23zM25 16h1v1H25zM27 16h2v1H27zM0 17h2v1H0zM7 17h1v1H7zM9 17h1v1H9zM21 17h1v1H21zM23 17h2v1H23zM26 17h1v1H26zM32,17 h1v1H32zM0 18h1v1H0zM3 18h2v1H3zM6 18h2v1H6zM21 18h2v1H21zM30 18h2v1H30zM0 19h2v1H0zM7 19h3v1H7zM21 19h1v1H21zM23 19h3v1H23zM28 19h4v1H28zM1 20h2v1H1zM6 20h2v1H6zM11 20h1v1H11zM22 20h1v1H22zM25 20h1v1H25zM27 20h3v1H27zM0 21h1v1H0zM2 21h1v1H2zM5 21h1v1H5zM7 21h1v1H7zM10 21h1v1H10zM15 21h1v1H15zM17 21h2v1H17zM20 21h2v1H20zM23 21h5v1H23zM29 21h2v1H29zM32,21 h1v1H32zM0 22h1v1H0zM2 22h2v1H2zM5 22h3v1H5zM9 22h1v1H9zM11 22h1v1H11zM18 22h1v1H18zM20 22h1v1H20zM24 22h1v1H24zM27 22h5v1H27zM0 23h1v1H0zM3 23h2v1H3zM9 23h4v1H9zM16 23h1v1H16zM18 23h1v1H18zM20 23h2v1H20zM23 23h2v1H23zM27 23h1v1H27zM29 23h3v1H29zM0 24h1v1H0zM3 24h1v1H3zM6 24h1v1H6zM8 24h2v1H8zM12 24h1v1H12zM14 24h1v1H14zM18 24h1v1H18zM20 24h1v1H20zM22 24h1v1H22zM24 24h5v1H24zM8 25h13v1H8zM24 25h1v1H24zM28 25h1v1H28zM32,25 h1v1H32zM0 26h7v1H0zM10 26h2v1H10zM13 26h3v1H13zM17 26h1v1H17zM19 26h2v1H19zM22 26h3v1H22zM26 26h1v1H26zM28 26h2v1H28zM31 26h1v1H31zM0 27h1v1H0zM6 27h1v1H6zM9 27h1v1H9zM11 27h1v1H11zM13 27h1v1H13zM16 27h1v1H16zM19 27h1v1H19zM23 27h2v1H23zM28 27h1v1H28zM30,27 h3v1H30zM0 28h1v1H0zM2 28h3v1H2zM6 28h1v1H6zM8 28h2v1H8zM12 28h1v1H12zM14 28h2v1H14zM18 28h1v1H18zM20 28h3v1H20zM24 28h5v1H24zM31,28 h2v1H31zM0 29h1v1H0zM2 29h3v1H2zM6 29h1v1H6zM8 29h2v1H8zM11 29h1v1H11zM16 29h1v1H16zM19 29h1v1H19zM21 29h1v1H21zM23 29h3v1H23zM28 29h1v1H28zM32,29 h1v1H32zM0 30h1v1H0zM2 30h3v1H2zM6 30h1v1H6zM8 30h4v1H8zM14 30h3v1H14zM18 30h1v1H18zM21 30h6v1H21zM29 30h1v1H29zM0 31h1v1H0zM6 31h1v1H6zM9 31h6v1H9zM17 31h3v1H17zM27 31h1v1H27zM30 31h1v1H30zM0 32h7v1H0zM9 32h1v1H9zM11 32h1v1H11zM14 32h2v1H14zM17 32h1v1H17zM20 32h1v1H20zM23 32h4v1H23zM29 32h1v1H29zM31 32h1v1H31z" shapeRendering="crispEdges"></path><image href="/img/forkit-icon.png" height="7" width="7" x="13" y="13" ></image></svg>
      </div>
    </div>
  </div>
  <p class="text-center text-3xl font-semibold">nuqs.47ng.com</p>
  <p class="text-center text-3xl font-semibold">Feedback</p>
</div>

