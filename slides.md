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
        Freelance Developer
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
Hello Rouen!

This is my first talk at a tech conference,<br/>
so please bear with me.
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
    <div class="text-5xl font-light text-zinc-500">
      Freelance Web Developer
    </div>
  </div>
</div>

<p class="text-center text-black dark:text-white text-5xl font-semibold mt-12">47ng.com/hi</p>

<!--
My name is François Best, I'm a freelance web developer since 2018.
-->

---
title: Before that
layout: image
image: /img/ssl.jpg
backgroundSize: fit
---

<!-- Before that, I used to work in the audio industry where we turned analog recording studio gear like this...
-->

---
title: Before that
layout: image
image: /img/vmr.jpg
backgroundSize: 120vh
---

<!-- ...into digital plugins using C++ -->

---

# 2016 {.text-center.-mt-12.mb-12}

<div class="grid grid-cols-3 gap-x-20 gap-y-2 text-xl text-center">
  <img src="/img/angular-js.png" width="150" height="150" class="block mx-auto"/>
  <img src="/img/react.png" width="150" height="150" class="block mx-auto"/>
  <img src="/img/vue.png" width="150" height="150" class="block mx-auto"/>
  <span>AngularJS</span>
  <span>React 16<br/><span class="text-zinc-500 text-base">(with Class Components)</span></span>
  <span>Vue 1</span>
</div>

<!-- I started using web technologies 8 years ago,
<br/>
when these started to become popular.
-->

---
title: The URL
---

<h1 class="text-6xl">The URL</h1>
<p class="text-4xl">
  <span class="text-cyan-500">https://</span>
  <span class="text-blue-500">example.com</span>
  <span class="text-green-500">/pathname</span>
  <span class="text-pink-500">?query=string</span>
  <span class="text-orange-500">#fragment</span>
</p>

The web's superpower

---
title: What we can do with URLs
---

- Share them
- Bookmark them

---
title: Pathname
---

<p class="text-4xl">
  <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span>
  <span class="text-green-500">/pathname</span>
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

<p class="text-4xl">
  <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span>
  <span class="text-zinc-500">/pathname</span>
  <span class="text-zinc-500">?query=string</span>
  <span class="text-orange-500">#fragment</span>
</p>

---
title: The Query string
---

<p class="text-4xl">
  <span class="text-zinc-500">https://</span>
  <span class="text-zinc-500">example.com</span>
  <span class="text-zinc-500">/pathname</span>
  <span class="text-black dark:text-white">?</span><span class="text-pink-500">query</span>=<span class="text-sky-500">string</span>
  <span class="text-zinc-500">#fragment</span>
</p>

---
title: Woodworking
layout: image
image: /img/dovetail-light.png
backgroundSize: contain
class: bg-white
---


---
title: Query string in Next.js
---

<p class="text-4xl text-black dark:text-white">In Next.js</p>

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

---
title: next-usequerystate
---

<h1 class="text-6xl">next-usequerystate</h1>

<p class="text-center">2020</p>

---
title: nuqs
---

<h1 class="text-9xl font-bold">
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

<h1 class="text-8xl text-center">Server-first</h1>

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

<h1 class="text-8xl text-center">History API</h1>

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

<h1 class="text-8xl text-center">Rate limits</h1>

---
title: Browsers
---

- Chrome: 50ms
- Firefox: 50ms
- Safari: 120ms

---
title: Throttling
---

<h1 class="text-8xl text-center">Throttling</h1>

---
title: Writing
---

<h1 class="text-8xl text-center">State &nbsp;→&nbsp; URL</h1>


---
title: Reading
---

<h1 class="text-8xl text-center">URL &nbsp;→&nbsp; State</h1>


---
title: Parsing
---

<h1 class="text-8xl text-center">Parsing</h1>

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

# The URL changes on…

- Initial load
- Client-side navigation
- Third party History updates
- `nuqs` updates

---
title: useSearchParams
---

<h1 class="text-7xl text-center">useSearchParams()</h1>

---
title: useSearchParams not reactive in older Next
---

<h1 class="text-7xl text-center"><span class="text-zinc-500 font-medium">(was)</span> Not reactive 😭</h1>

---
title: Patching globals
---

<h1 class="text-7xl text-center">Patching history 😱</h1>

---

```tsx
history.pushState(state, '', url)
```

<style>
pre, code {
  font-size: 2rem;
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

- Parsers can be expensive
- Parsing on every change is wasteful
- We already have the JS values!

---
title: Sync
---

<h1 class="text-8xl text-center">Syncing via<br/>Event Emitter</h1>

---
title: Bug on canary
---

<blockquote class="italic text-4xl">"I have a bug with Next.js <strong>canary</strong>"</blockquote>

---
title: MIT license
---

```
THE SOFTWARE IS PROVIDED "AS IS",
WITHOUT WARRANTY OF ANY KIND
```

<style>
pre, code {
  font-size: 2rem;
}
</style>

---
title: What I like
---

<div class="text-black dark:text-white text-6xl font-medium leading-relaxed">

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

<h1 class="text-8xl text-center">What are<br/>our options?</h1>

---
title: GitHub API
---

<h1 class="text-8xl text-center">GitHub API</h1>

---
title: Cron
---

<h1 class="text-8xl text-center flex items-center gap-2"><img src="/img/raspberry-pi.svg" class="h-32 -mt-6 inline-block"/> Cron &nbsp;→&nbsp; CI <img src="/img/gha.svg" class="h-32 inline-block ml-4"/></h1>

---
title: Testing
---

<h1 class="text-8xl text-center">🧪 Testing</h1>

---
title: Good tests are the only way to stay sane
---

<blockquote class="text-8xl text-center italic font-bold text-black dark:text-white leading-tight"><span class="text-zinc-500">"</span>Good tests are<br/>the only way<br/>to stay sane<span class="text-zinc-500">"</span></blockquote>

---
title: Behaviour coverage
---

<h1 class="text-8xl text-center"><strike class="text-zinc-500 font-medium">code</strike> behaviour coverage</h1>

---
title: Next.js issues
---

<div class="text-black dark:text-white text-4xl font-medium leading-relaxed">

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

<h1 class="text-8xl text-center">Golden rule<br/>of testing</h1>

---

<blockquote class="p-12 text-6xl text-center italic font-semibold text-black dark:text-white leading-tight"><span class="text-zinc-500">"</span>A test must fail if, and only if, the <span class="font-extrabold">intention</span> behind the system is not met.<span class="text-zinc-500">"</span></blockquote>

<p class="text-right mr-10 text-2xl">Artem Zakharchenko<br/><a href="https://x.com/kettanaito" class="font-medium">@kettanaito</a></p>

---
title: Depending on internals
---

<h1 class="text-8xl text-center leading-tight">Depending on internals</h1>

---
title: Beyoncé rule of software
---

<h1 class="text-8xl text-center leading-tight">Beyoncé rule<br/>of software</h1>

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

<h1 class="text-8xl text-center">
End-to-end<br/>testing
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

<h1 class="text-7xl text-center">Testing<br/>every<br/>supported<br/>version</h1>

<p class="text-center text-zinc-500 text-4xl font-semibold mt-20">With variants</p>


---
title: Thanks Turborepo
---

<svg class="h-48 mr-12" fill="none" viewBox="0 0 120 28" xmlns="http://www.w3.org/2000/svg"><title>Turborepo</title><defs><linearGradient gradientUnits="userSpaceOnUse" id="logo-ring-gradient" x1="15.0234" x2="3.64419" y1="4.00556" y2="15.3847"><stop stop-color="#0096FF"></stop><stop offset="1" stop-color="#FF1E56"></stop></linearGradient><linearGradient id="gradient"><stop offset="0%" stop-color="#000000"></stop><stop offset="25%" stop-color="#ffffff"></stop><stop offset="85%" stop-color="#ffffff"></stop><stop offset="100%" stop-color="#000000"></stop></linearGradient><mask id="logo-mask"><rect fill="url(#gradient)" height="26" transform="translate(-8,0)" width="46" x="0" y="0"></rect></mask></defs><g mask="url(#logo-mask)" transform="translate(8,0)"><g class="relative z-0" opacity="1" style="transform: none; transform-origin: 13.9488px 13.9398px 0px;" transform-origin="13.948790550231934px 13.939799308776855px"><path class="fill-black dark:fill-white" d="M13.9396 6.42181C9.79423 6.42181 6.42163 9.79441 6.42163 13.9398C6.42163 18.0852 9.79423 21.4578 13.9396 21.4578C18.085 21.4578 21.4576 18.0852 21.4576 13.9398C21.4576 9.79441 18.085 6.42181 13.9396 6.42181ZM13.9396 17.8304C11.7906 17.8304 10.049 16.0888 10.049 13.9398C10.049 11.7908 11.7906 10.0492 13.9396 10.0492C16.0886 10.0492 17.8302 11.7908 17.8302 13.9398C17.8302 16.0888 16.0886 17.8304 13.9396 17.8304Z"></path><path clip-rule="evenodd" d="M14.5697 5.187V2.38C20.6709 2.7062 25.5177 7.7574 25.5177 13.9398C25.5177 20.1222 20.6709 25.172 14.5697 25.4996V22.6926C19.1169 22.3678 22.7177 18.5682 22.7177 13.9398C22.7177 9.3114 19.1169 5.5118 14.5697 5.187ZM7.30928 19.6798C6.10388 18.2882 5.32688 16.5158 5.18828 14.5698H2.37988C2.52548 17.2928 3.61468 19.7638 5.32128 21.6664L7.30788 19.6798H7.30928ZM13.3097 25.4996V22.6926C11.3623 22.554 9.5899 21.7784 8.1983 20.5716L6.2117 22.5582C8.1157 24.2662 10.5867 25.354 13.3083 25.4996H13.3097Z" fill="url(#logo-ring-gradient)" fill-rule="evenodd"></path></g></g><g class="relative z-10 header-logo_desktopLogo__zIjld" transform="translate(8,0)"><path class="fill-black dark:fill-white" d="M48.2623 11.2944V8.24418H33.5623V11.2944H39.1115V21.4374H42.713V11.2944H48.2623Z"></path><path class="fill-black dark:fill-white" d="M56.5679 21.6396C61.0882 21.6396 63.5688 19.3427 63.5688 15.5574V8.24418H59.9673V15.2083C59.9673 17.3214 58.8648 18.5158 56.5679 18.5158C54.271 18.5158 53.1685 17.3214 53.1685 15.2083V8.24418H49.567V15.5574C49.567 19.3427 52.0476 21.6396 56.5679 21.6396Z"></path><path class="fill-black dark:fill-white" d="M69.0819 17.0642H72.665L75.4947 21.4374H79.6291L76.4319 16.6783C78.2326 16.0352 79.3351 14.6019 79.3351 12.6542C79.3351 9.82443 77.222 8.24418 74.0064 8.24418H65.4804V21.4374H69.0819V17.0642ZM69.0819 14.2161V11.2577H73.8226C75.0905 11.2577 75.7887 11.8089 75.7887 12.7461C75.7887 13.6281 75.0905 14.2161 73.8226 14.2161H69.0819Z"></path><path class="fill-black dark:fill-white" d="M81.0108 21.4374H90.4372C93.3772 21.4374 95.0677 20.0409 95.0677 17.7073C95.0677 16.1454 94.0754 15.0797 92.8994 14.6019C93.7079 14.2161 94.7002 13.2973 94.7002 11.8457C94.7002 9.51206 93.0464 8.24418 90.1248 8.24418H81.0108V21.4374ZM84.4653 13.4076V11.1658H89.7573C90.7496 11.1658 91.3008 11.5517 91.3008 12.2867C91.3008 13.0217 90.7496 13.4076 89.7573 13.4076H84.4653ZM84.4653 16.1087H90.0881C91.0619 16.1087 91.5948 16.5864 91.5948 17.3031C91.5948 18.0197 91.0619 18.4974 90.0881 18.4974H84.4653V16.1087Z"></path><path class="fill-black dark:fill-white" d="M103.873 8.02368C99.2612 8.02368 95.9353 10.9086 95.9353 14.8408C95.9353 18.7731 99.2612 21.6579 103.873 21.6579C108.485 21.6579 111.793 18.7731 111.793 14.8408C111.793 10.9086 108.485 8.02368 103.873 8.02368ZM103.873 11.1474C106.299 11.1474 108.118 12.5807 108.118 14.8408C108.118 17.1009 106.299 18.5342 103.873 18.5342C101.448 18.5342 99.6287 17.1009 99.6287 14.8408C99.6287 12.5807 101.448 11.1474 103.873 11.1474Z"></path></g></svg>

---
title: Announcement
---

- React 19
- Next.js 15
- nuqs 2

---
title: v2 Features
---

- Smaller bundle size
- ESM only
- (maybe) no more patching internals
- fewer hacks

---
title: Thank you!
---

<h1 class="text-8xl text-center">Thank you!</h1>

<p class="text-center text-6xl font-semibold mt-12"><a href="https://nuqs.47ng.com">nuqs.47ng.com</a></p>
