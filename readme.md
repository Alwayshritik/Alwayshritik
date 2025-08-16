<!doctype html>

<html lang="en" class="scroll-smooth">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Ritik Jha — Web Developer & SEO</title>
  <meta name="description" content="Portfolio website for Ritik Jha — Frontend Developer, SEO & Digital Creative." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
  <!-- Tailwind via CDN (for quick GitHub Pages deployment). Replace with a build setup if needed. -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    // Tailwind config
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: { sans: ['Inter', 'ui-sans-serif', 'system-ui'] },
          colors: {
            brand: {
              50: '#eef9ff',
              100: '#d9f1ff',
              200: '#b6e4ff',
              300: '#84d1ff',
              400: '#49b8ff',
              500: '#1e9bff',
              600: '#0a7be6',
              700: '#075fb8',
              800: '#084f91',
              900: '#0a446f'
            }
          },
          boxShadow: {
            soft: '0 10px 30px -12px rgba(2,6,23,0.35)'
          }
        }
      }
    }
  </script>
  <style>
    /* subtle animated underline for nav */
    .nav-link{position:relative}
    .nav-link:after{content:'';position:absolute;left:0;bottom:-6px;height:2px;width:0;background:currentColor;transition:width .25s ease}
    .nav-link:hover:after,.nav-link[aria-current="page"]:after{width:100%}
    /* marquee */
    .marquee{white-space:nowrap;overflow:hidden}
    .marquee-inner{display:inline-block;will-change:transform;animation:marquee 22s linear infinite}
    @keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
  </style>
</head>
<body class="bg-white text-slate-800 dark:bg-slate-950 dark:text-slate-100 font-sans">
  <!-- Sticky Nav -->
  <header class="sticky top-0 z-50 backdrop-blur supports-[backdrop-filter]:bg-white/70 dark:supports-[backdrop-filter]:bg-slate-900/60 border-b border-slate-200/60 dark:border-slate-800">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 flex items-center justify-between h-16">
      <a href="#home" class="font-extrabold tracking-tight text-xl">Ritik<span class="text-brand-600">.</span>Jha</a>
      <nav class="hidden md:flex items-center gap-8 text-sm">
        <a class="nav-link" href="#portfolio">Portfolio</a>
        <a class="nav-link" href="#about">About</a>
        <a class="nav-link" href="#services">Services</a>
        <a class="nav-link" href="#resume">Resume</a>
        <a class="nav-link" href="#contact">Contact</a>
      </nav>
      <div class="flex items-center gap-3">
        <a href="#contact" class="hidden sm:inline-block rounded-2xl bg-brand-600 px-4 py-2 text-white font-medium shadow-soft hover:bg-brand-700">Let's Talk</a>
        <button id="themeToggle" class="p-2 rounded-xl border border-slate-200 dark:border-slate-800" aria-label="Toggle theme">
          <svg id="sun" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 block dark:hidden" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="4"/><path d="M12 2v2m0 16v2M4 12H2m20 0h-2M5 5l-1.4-1.4M19.4 19.4 18 18M19 5l1.4-1.4M5 19 3.6 20.4"/></svg>
          <svg id="moon" xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 hidden dark:block" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
        </button>
        <button id="menuBtn" class="md:hidden p-2 rounded-xl border border-slate-200 dark:border-slate-800" aria-label="Open menu">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M3 12h18M3 6h18M3 18h18"/></svg>
        </button>
      </div>
    </div>
    <!-- mobile menu -->
    <div id="mobileMenu" class="md:hidden hidden border-t border-slate-200 dark:border-slate-800">
      <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-3 flex flex-col gap-3">
        <a class="nav-link" href="#portfolio" onclick="closeMenu()">Portfolio</a>
        <a class="nav-link" href="#about" onclick="closeMenu()">About</a>
        <a class="nav-link" href="#services" onclick="closeMenu()">Services</a>
        <a class="nav-link" href="#resume" onclick="closeMenu()">Resume</a>
        <a class="nav-link" href="#contact" onclick="closeMenu()">Contact</a>
      </div>
    </div>
  </header>  <!-- Hero -->  <section id="home" class="relative overflow-hidden">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 grid lg:grid-cols-2 gap-10 items-center py-16">
      <div>
        <p class="text-sm tracking-widest uppercase text-brand-700 font-semibold">Based in India</p>
        <h1 class="mt-3 text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight">
          I'm <span class="text-brand-600">Ritik Jha</span><br />
          Frontend Developer • SEO • Creative Strategist
        </h1>
        <p class="mt-6 text-slate-600 dark:text-slate-300 max-w-2xl">I design and build fast, accessible websites that convert. Clean UI, modern performance, and search-friendly foundations — all crafted to grow your brand.</p>
        <div class="mt-8 flex flex-wrap gap-3">
          <a href="#portfolio" class="rounded-2xl bg-slate-900 text-white dark:bg-white dark:text-slate-900 px-5 py-3 font-semibold shadow-soft">My Works</a>
          <a href="#contact" class="rounded-2xl border border-slate-300 dark:border-slate-700 px-5 py-3 font-semibold">Hire Me</a>
          <a href="./Ritik-Jha-CV.pdf" class="rounded-2xl border border-slate-300 dark:border-slate-700 px-5 py-3 font-semibold" download>Download CV</a>
        </div>
        <div class="mt-10 marquee">
          <div class="marquee-inner text-sm opacity-70">
            <span class="mx-6">HTML5</span><span class="mx-6">CSS3</span><span class="mx-6">Tailwind</span><span class="mx-6">JavaScript</span><span class="mx-6">React</span><span class="mx-6">Next.js</span><span class="mx-6">WordPress</span><span class="mx-6">SEO</span>
            <span class="mx-6">Shopify</span><span class="mx-6">GA4</span><span class="mx-6">GTM</span><span class="mx-6">SQL</span>
            <!-- duplicate for seamless loop -->
            <span class="mx-6">HTML5</span><span class="mx-6">CSS3</span><span class="mx-6">Tailwind</span><span class="mx-6">JavaScript</span><span class="mx-6">React</span><span class="mx-6">Next.js</span><span class="mx-6">WordPress</span><span class="mx-6">SEO</span>
            <span class="mx-6">Shopify</span><span class="mx-6">GA4</span><span class="mx-6">GTM</span><span class="mx-6">SQL</span>
          </div>
        </div>
      </div>
      <div class="relative">
        <div class="aspect-square rounded-[2rem] bg-gradient-to-br from-brand-100 to-brand-300 dark:from-slate-800 dark:to-slate-700 p-2">
          <div class="w-full h-full rounded-[1.7rem] bg-[url('https://images.unsplash.com/photo-1544723795-3fb6469f5b39?q=80&w=1200&auto=format&fit=crop')] bg-cover bg-center"></div>
        </div>
        <div class="absolute -bottom-6 -left-6 hidden sm:block">
          <div class="rounded-2xl bg-white dark:bg-slate-900 shadow-soft px-4 py-3">
            <p class="text-xs uppercase tracking-wide text-slate-500">Experience</p>
            <p class="font-bold text-lg">2+ Years</p>
          </div>
        </div>
      </div>
    </div>
  </section>  <!-- Portfolio -->  <section id="portfolio" class="py-16 border-t border-slate-200/60 dark:border-slate-800">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="flex items-end justify-between gap-6 flex-wrap">
        <div>
          <h2 class="text-3xl sm:text-4xl font-extrabold">Recent Projects</h2>
          <p class="mt-2 text-slate-600 dark:text-slate-300">A few highlights — clean, responsive, and conversion-focused.</p>
        </div>
        <a href="#contact" class="rounded-2xl bg-brand-600 px-4 py-2 text-white font-medium shadow-soft hover:bg-brand-700">Work with me</a>
      </div><div class="mt-10 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
    <!-- Card template -->
    <article class="group rounded-2xl overflow-hidden border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 shadow-soft">
      <a href="#" class="block">
        <div class="aspect-[16/10] bg-[url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1200&auto=format&fit=crop')] bg-cover bg-center"></div>
      </a>
      <div class="p-5">
        <p class="text-xs uppercase tracking-wide text-brand-700 font-semibold">Web App</p>
        <h3 class="mt-1 text-lg font-bold">AI Startup Landing Page</h3>
        <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Built with Next.js and Tailwind, optimized for speed and SEO. Clean illustrations and clear CTAs drive sign‑ups.</p>
        <div class="mt-4 flex items-center gap-3 text-xs"><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Next.js</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Tailwind</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Vercel</span></div>
      </div>
    </article>
    <article class="group rounded-2xl overflow-hidden border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 shadow-soft">
      <a href="#" class="block">
        <div class="aspect-[16/10] bg-[url('https://images.unsplash.com/photo-1545239351-1141bd82e8a6?q=80&w=1200&auto=format&fit=crop')] bg-cover bg-center"></div>
      </a>
      <div class="p-5">
        <p class="text-xs uppercase tracking-wide text-brand-700 font-semibold">E‑commerce</p>
        <h3 class="mt-1 text-lg font-bold">Saree Brand Store</h3>
        <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">WooCommerce theme customization, schema, and Core Web Vitals tuning for better conversions.</p>
        <div class="mt-4 flex items-center gap-3 text-xs"><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">WordPress</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Woo</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">SEO</span></div>
      </div>
    </article>
    <article class="group rounded-2xl overflow-hidden border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 shadow-soft">
      <a href="#" class="block">
        <div class="aspect-[16/10] bg-[url('https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?q=80&w=1200&auto=format&fit=crop')] bg-cover bg-center"></div>
      </a>
      <div class="p-5">
        <p class="text-xs uppercase tracking-wide text-brand-700 font-semibold">Marketing</p>
        <h3 class="mt-1 text-lg font-bold">Digital Agency Site</h3>
        <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Elementor + custom code, GA4 & GTM tracking, and landing pages that convert.</p>
        <div class="mt-4 flex items-center gap-3 text-xs"><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Elementor</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">GA4</span><span class="px-2 py-1 rounded-full bg-slate-100 dark:bg-slate-800">GTM</span></div>
      </div>
    </article>
  </div>
</div>

  </section>  <!-- About & Stats -->  <section id="about" class="py-16">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 grid lg:grid-cols-2 gap-12 items-start">
      <div>
        <h2 class="text-3xl sm:text-4xl font-extrabold">About Me</h2>
        <p class="mt-4 text-slate-600 dark:text-slate-300">I’m a frontend developer and SEO practitioner focused on performance, accessibility, and clean design. I partner with startups, creators, and local businesses to ship websites that look great and deliver measurable results.</p>
        <dl class="mt-8 grid grid-cols-3 gap-4">
          <div class="rounded-2xl bg-slate-100 dark:bg-slate-800 p-5 text-center"><dt class="text-3xl font-extrabold">40+</dt><dd class="text-xs opacity-70 mt-1">Projects</dd></div>
          <div class="rounded-2xl bg-slate-100 dark:bg-slate-800 p-5 text-center"><dt class="text-3xl font-extrabold">39+</dt><dd class="text-xs opacity-70 mt-1">Happy Clients</dd></div>
          <div class="rounded-2xl bg-slate-100 dark:bg-slate-800 p-5 text-center"><dt class="text-3xl font-extrabold">2+</dt><dd class="text-xs opacity-70 mt-1">Years</dd></div>
        </dl>
      </div>
      <div class="space-y-6">
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold text-lg">What I do</h3>
          <ul class="mt-3 grid sm:grid-cols-2 gap-3 text-sm list-disc pl-5">
            <li>Website & Web‑App Development (React, Next.js, WordPress)</li>
            <li>SEO Strategy (On‑page, Technical, Schema, Backlinks)</li>
            <li>eCommerce (Shopify & WooCommerce)</li>
            <li>Design & Content (social posts, thumbnails, brand assets)</li>
          </ul>
        </div>
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold text-lg">Contact Info</h3>
          <dl class="mt-3 grid sm:grid-cols-2 gap-x-6 gap-y-3 text-sm">
            <div><dt class="text-slate-500">Name</dt><dd class="font-medium">Ritik Jha</dd></div>
            <div><dt class="text-slate-500">Location</dt><dd class="font-medium">Greater Noida, India</dd></div>
            <div><dt class="text-slate-500">Phone</dt><dd class="font-medium">+91 00000 00000</dd></div>
            <div><dt class="text-slate-500">Email</dt><dd class="font-medium">hello.ritikjha@email.com</dd></div>
          </dl>
        </div>
      </div>
    </div>
  </section>  <!-- Services -->  <section id="services" class="py-16 border-t border-slate-200/60 dark:border-slate-800">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl sm:text-4xl font-extrabold">Services</h2>
      <div class="mt-8 grid md:grid-cols-2 xl:grid-cols-4 gap-6">
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold">Website Development</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">WordPress, Shopify, custom React/Next.js — fast, responsive, and built to convert.</p>
        </div>
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold">SEO & Analytics</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">On‑page, technical SEO, schema, GA4/GTM tracking, and growth reporting.</p>
        </div>
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold">Graphic Design</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Brand assets, social graphics, banners, brochures, and thumbnails.</p>
        </div>
        <div class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6">
          <h3 class="font-bold">Short‑form Video</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-300">Reels/Shorts concepts, editing, hooks, captions, and effects that catch attention.</p>
        </div>
      </div>
    </div>
  </section>  <!-- Resume -->  <section id="resume" class="py-16">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl sm:text-4xl font-extrabold">Resume</h2>
      <div class="mt-8 grid lg:grid-cols-2 gap-10">
        <div>
          <h3 class="text-xl font-bold">Education</h3>
          <ol class="mt-4 space-y-5">
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2022 – 2026</p>
              <p class="font-semibold">B.Tech, Computer Science & Engineering</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">Galgotias University</p>
            </li>
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2020 – 2022</p>
              <p class="font-semibold">Higher Secondary Certificate</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">St. Michael's School</p>
            </li>
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2020</p>
              <p class="font-semibold">Secondary School Certificate</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">St. Michael's School</p>
            </li>
          </ol>
        </div>
        <div>
          <h3 class="text-xl font-bold">Experience</h3>
          <ol class="mt-4 space-y-5">
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2024 – Present</p>
              <p class="font-semibold">Website Developer — WebWorks.co Pvt. Ltd.</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">Building high‑performance websites with a focus on UX, SEO, and conversions.</p>
            </li>
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2023 – 2024</p>
              <p class="font-semibold">Frontend Developer — Dream Provider Pvt. Ltd.</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">Collaborated with backend teams to ship responsive UIs and design systems.</p>
            </li>
            <li class="rounded-2xl border border-slate-200 dark:border-slate-800 p-5">
              <p class="text-sm text-slate-500">2022 – 2023</p>
              <p class="font-semibold">UI/UX Designer — Tophawks Agency</p>
              <p class="text-sm text-slate-600 dark:text-slate-300">Wireframes, prototypes, and polished designs for web and mobile products.</p>
            </li>
          </ol>
        </div>
      </div><div class="mt-10">
    <h3 class="text-xl font-bold">Tech Stack</h3>
    <div class="mt-4 flex flex-wrap gap-2 text-sm">
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">HTML5</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">CSS3</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Tailwind</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">JavaScript</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">React</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Next.js</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">WordPress</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Shopify</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">GA4</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">GTM</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">SQL</span>
      <span class="px-3 py-1 rounded-full bg-slate-100 dark:bg-slate-800">Git & GitHub</span>
    </div>
  </div>
</div>

  </section>  <!-- Testimonials -->  <section id="testimonials" class="py-16 border-t border-slate-200/60 dark:border-slate-800">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <h2 class="text-3xl sm:text-4xl font-extrabold">Clients say</h2>
      <div class="mt-8 grid md:grid-cols-2 xl:grid-cols-3 gap-6">
        <figure class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6 bg-white dark:bg-slate-900">
          <blockquote class="text-sm text-slate-700 dark:text-slate-300">“From logo to website, Ritik delivered high‑quality work that fit our brand perfectly. Reliable and creative.”</blockquote>
          <figcaption class="mt-4 text-xs text-slate-500">— Apex Media</figcaption>
        </figure>
        <figure class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6 bg-white dark:bg-slate-900">
          <blockquote class="text-sm text-slate-700 dark:text-slate-300">“Our store performance improved significantly after his SEO and speed optimizations. Highly recommended.”</blockquote>
          <figcaption class="mt-4 text-xs text-slate-500">— Saree Brand Owner</figcaption>
        </figure>
        <figure class="rounded-2xl border border-slate-200 dark:border-slate-800 p-6 bg-white dark:bg-slate-900">
          <blockquote class="text-sm text-slate-700 dark:text-slate-300">“Clean design, fast delivery, measurable results. Exactly what we needed.”</blockquote>
          <figcaption class="mt-4 text-xs text-slate-500">— WebWorks.co</figcaption>
        </figure>
      </div>
    </div>
  </section>  <!-- Contact -->  <section id="contact" class="py-16">
    <div class="mx-auto max-w-3xl px-4 sm:px-6 lg:px-8">
      <div class="rounded-3xl border border-slate-200 dark:border-slate-800 p-8 bg-white dark:bg-slate-900 shadow-soft">
        <h2 class="text-3xl sm:text-4xl font-extrabold">Got a project in mind?</h2>
        <p class="mt-2 text-slate-600 dark:text-slate-300">Send a message — I’ll reply within 24 hours. For urgent queries, reach me on WhatsApp.</p>
        <form name="contact" method="POST" data-netlify="true" class="mt-8 grid gap-4">
          <input type="hidden" name="form-name" value="contact" />
          <input required name="name" placeholder="Your name" class="rounded-2xl border border-slate-300 dark:border-slate-700 bg-transparent px-4 py-3" />
          <input required type="email" name="email" placeholder="Your email" class="rounded-2xl border border-slate-300 dark:border-slate-700 bg-transparent px-4 py-3" />
          <input name="phone" placeholder="Phone (optional)" class="rounded-2xl border border-slate-300 dark:border-slate-700 bg-transparent px-4 py-3" />
          <textarea required name="message" rows="5" placeholder="Tell me about your project" class="rounded-2xl border border-slate-300 dark:border-slate-700 bg-transparent px-4 py-3"></textarea>
          <div class="flex items-center gap-3">
            <button class="rounded-2xl bg-brand-600 px-5 py-3 text-white font-semibold shadow-soft hover:bg-brand-700" type="submit">Send Message</button>
            <a href="https://wa.me/910000000000" class="text-sm underline">WhatsApp</a>
          </div>
        </form>
      </div><footer class="mt-10 text-center text-sm text-slate-500">
    <p>© <span id="year"></span> Ritik Jha — Web Developer & SEO Specialist</p>
  </footer>
</div>

  </section>  <script>
    // Theme toggle with localStorage
    const root = document.documentElement;
    const themeToggle = document.getElementById('themeToggle');
    const mobileMenu = document.getElementById('mobileMenu');
    const menuBtn = document.getElementById('menuBtn');

    function setTheme(dark){ dark ? root.classList.add('dark') : root.classList.remove('dark'); localStorage.setItem('theme', dark ? 'dark' : 'light'); }
    (function(){
      const saved = localStorage.getItem('theme');
      if(saved){ setTheme(saved === 'dark'); }
      else if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches){ setTheme(true); }
      document.getElementById('year').textContent = new Date().getFullYear();
    })();

    themeToggle.addEventListener('click', ()=> setTheme(!root.classList.contains('dark')));
    menuBtn.addEventListener('click', ()=> mobileMenu.classList.toggle('hidden'));
    window.closeMenu = ()=> mobileMenu.classList.add('hidden');
  </script></body>
</html>