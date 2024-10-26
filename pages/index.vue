<template>
    <div 
        class="max-w-full h-full bg-slate-900 leading-relaxed text-slate-400 antialiased selection:bg-teal-300 selection:text-teal-900"
        @mousemove="updateBackground" ref="backgroundDiv">
        <div
            class="pointer-events-none fixed inset-0 z-30 transition duration-300 lg:absolute"
            :style="backgroundStyle"
        ></div>
        <div class="mx-auto min-h-screen max-w-screen-xl flex justify-between px-6 py-12 font-sans md:px-12 md:py-20 lg:px-24 lg:py-0 gap-4">
            <header class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg:flex-col lg:justify-between lg:py-24">
                <div>
                    <h1 class="text-slate-200 text-4xl font-bold">Kornkawee Songyen</h1>
                    <h2 class="text-slate-200 text-lg font-semibold">Software Engineer</h2>
                    <p class="text-slate-200 text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. In temporibus laboriosam consequuntur pariatur reiciendis quia consectetur obcaecati! Similique atque non illo explicabo eligendi tempore. Magni accusamus laborum distinctio vel autem.</p>
                    <nav class="nav hidden lg:block" aria-label="In-page jump links">
                        <ul class="w-max">
                            <li><a class="group flex items-center py-3" href="#about">
                                <span class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"></span>
                                <span class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200">About</span>
                                </a>
                            </li>
                            <li><a class="group flex items-center py-3" href="#experience">
                                <span class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"></span>
                                <span class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200">Experience</span>
                                </a>
                            </li>
                            <li><a class="group flex items-center py-3" href="#projects">
                                <span class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"></span>
                                <span class="nav-text text-xs font-bold uppercase tracking-widest text-slate-500 group-hover:text-slate-200 group-focus-visible:text-slate-200">Project</span>
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
                <ul class="ml-1 mt-8 flex items-center">
                    <li class="mr-5 text-xs shrink-0">
                        <a href="https://github.com/KornkaweeSY">
                            <svg xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 24 24"><mask id="lineMdGithubLoop0" width="24" height="24" x="0" y="0"><g fill="#fff"><ellipse cx="9.5" cy="9" rx="1.5" ry="1"/><ellipse cx="14.5" cy="9" rx="1.5" ry="1"/></g></mask><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path stroke-dasharray="32" stroke-dashoffset="32" d="M12 4c1.67 0 2.61 0.4 3 0.5c0.53 -0.43 1.94 -1.5 3.5 -1.5c0.34 1 0.29 2.22 0 3c0.75 1 1 2 1 3.5c0 2.19 -0.48 3.58 -1.5 4.5c-1.02 0.92 -2.11 1.37 -3.5 1.5c0.65 0.54 0.5 1.87 0.5 2.5c0 0.73 0 3 0 3M12 4c-1.67 0 -2.61 0.4 -3 0.5c-0.53 -0.43 -1.94 -1.5 -3.5 -1.5c-0.34 1 -0.29 2.22 0 3c-0.75 1 -1 2 -1 3.5c0 2.19 0.48 3.58 1.5 4.5c1.02 0.92 2.11 1.37 3.5 1.5c-0.65 0.54 -0.5 1.87 -0.5 2.5c0 0.73 0 3 0 3"><animate fill="freeze" attributeName="stroke-dashoffset" dur="0.7s" values="32;0"/></path><path stroke-dasharray="10" stroke-dashoffset="10" d="M9 19c-1.406 0-2.844-.563-3.688-1.188C4.47 17.188 4.22 16.157 3 15.5"><animate attributeName="d" dur="3s" repeatCount="indefinite" values="M9 19c-1.406 0-2.844-.563-3.688-1.188C4.47 17.188 4.22 16.157 3 15.5;M9 19c-1.406 0-3-.5-4-.5-.532 0-1 0-2-.5;M9 19c-1.406 0-2.844-.563-3.688-1.188C4.47 17.188 4.22 16.157 3 15.5"/><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.8s" dur="0.2s" values="10;0"/></path></g><rect width="8" height="4" x="8" y="11" fill="currentColor" mask="url(#lineMdGithubLoop0)"><animate attributeName="y" dur="10s" keyTimes="0;0.45;0.46;0.54;0.55;1" repeatCount="indefinite" values="11;11;7;7;11;11"/></rect></svg>                        
                        </a>
                    </li>
                    <li class="mr-5 text-xs shrink-0">
                        <a href="">
                            <svg xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 24 24"><circle cx="4" cy="4" r="2" fill="currentColor" fill-opacity="0"><animate fill="freeze" attributeName="fill-opacity" dur="0.15s" values="0;1"/></circle><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"><path stroke-dasharray="12" stroke-dashoffset="12" d="M4 10v10"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.15s" dur="0.2s" values="12;0"/></path><path stroke-dasharray="12" stroke-dashoffset="12" d="M10 10v10"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.45s" dur="0.2s" values="12;0"/></path><path stroke-dasharray="24" stroke-dashoffset="24" d="M10 15c0 -2.76 2.24 -5 5 -5c2.76 0 5 2.24 5 5v5"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.65s" dur="0.2s" values="24;0"/></path></g></svg>                        
                        </a>
                    </li>
                    <li class="mr-5 text-xs shrink-0">
                        <a href="">
                            <svg xmlns="http://www.w3.org/2000/svg" width="2em" height="2em" viewBox="0 0 24 24"><circle cx="17" cy="7" r="1.5" fill="currentColor" fill-opacity="0"><animate fill="freeze" attributeName="fill-opacity" begin="1.3s" dur="0.15s" values="0;1"/></circle><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path stroke-dasharray="72" stroke-dashoffset="72" d="M16 3c2.76 0 5 2.24 5 5v8c0 2.76 -2.24 5 -5 5h-8c-2.76 0 -5 -2.24 -5 -5v-8c0 -2.76 2.24 -5 5 -5h4Z"><animate fill="freeze" attributeName="stroke-dashoffset" dur="0.6s" values="72;0"/></path><path stroke-dasharray="28" stroke-dashoffset="28" d="M12 8c2.21 0 4 1.79 4 4c0 2.21 -1.79 4 -4 4c-2.21 0 -4 -1.79 -4 -4c0 -2.21 1.79 -4 4 -4"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.7s" dur="0.6s" values="28;0"/></path></g></svg>                        
                        </a>
                    </li>
                </ul>
            </header>
            <main class="lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg: flex-col lg:justify-between lg:py-24 overscroll-y-auto">
                <section id="about" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24" aria-label="About me">
                    <div class="sticky top-0 z-20 -mx-6 mb-4 w-screen bg-slate-900/75 px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0">
                        <h2 class="text-sm font-bold uppercase tracking-widest text-slate-200 lg:sr-only">About</h2>
                    </div>
                    <div>
                        <p class="mb-4">Back in 2012, I decided to try my hand at creating custom Tumblr themes and tumbled head first into the rabbit hole of coding and web development. Fast-forward to today, and I’ve had the privilege of building software for an
                            <a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://us.mullenlowe.com/" target="_blank" rel="noreferrer noopener" aria-label="advertising agency (opens in a new tab)">advertising agency</a>
                            , a<a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://starry.com/" target="_blank" rel="noreferrer noopener" aria-label="start-up (opens in a new tab)">start-up</a>
                            , a<a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://www.apple.com/apple-music/" target="_blank" rel="noreferrer noopener" aria-label="huge corporation (opens in a new tab)">huge corporation</a>
                            , and a<!-- --> <a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://upstatement.com/" target="_blank" rel="noreferrer noopener" aria-label="digital product studio (opens in a new tab)">digital product studio</a>
                            .</p><p class="mb-4">My main focus these days is building accessible user interfaces for our customers at<a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://www.klaviyo.com/" target="_blank" rel="noreferrer noopener" aria-label="Klaviyo (opens in a new tab)">Klaviyo</a>
                            . I most enjoy building software in the sweet spot where design and engineering meet — things that look good but are also built well under the hood. In my free time, I've also released an
                            <a class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300" href="https://www.newline.co/courses/build-a-spotify-connected-app" target="_blank" rel="noreferrer noopener" aria-label="online video course (opens in a new tab)">online video course</a> 
                            <!-- -->that covers everything you need to know to build a web app with the Spotify API.</p>
                             <p>When I’m not at the computer, I’m usually rock climbing, reading, hanging out with my wife and two cats, or running around Hyrule searching for<!-- --> 
                                <span class="group/korok inline-flex lg:cursor-[url('/images/koroks/Elma.png'),_pointer] lg:font-medium lg:text-slate-200"><span class="sr-only">Korok seeds</span>
                                <span class="group-hover/korok:text-red-400 transition duration-75 group-hover/korok:-translate-y-px delay-[50ms]" aria-hidden="true">K</span>
                                <span class="group-hover/korok:text-orange-400 transition duration-75 group-hover/korok:-translate-y-px delay-[75ms]" aria-hidden="true">o</span>
                                <span class="group-hover/korok:text-yellow-400 transition duration-75 group-hover/korok:-translate-y-px delay-[100ms]" aria-hidden="true">r</span>
                                <span class="group-hover/korok:text-lime-400 transition duration-75 group-hover/korok:-translate-y-px delay-[125ms]" aria-hidden="true">o</span>
                                <span class="group-hover/korok:text-green-400 transition duration-75 group-hover/korok:-translate-y-px delay-[150ms]" aria-hidden="true">k</span>
                                <span class="group-hover/korok:text-teal-400 transition duration-75 group-hover/korok:-translate-y-px delay-[175ms]" aria-hidden="true">&nbsp;</span>
                                <span class="group-hover/korok:text-cyan-400 transition duration-75 group-hover/korok:-translate-y-px delay-[200ms]" aria-hidden="true">s</span>
                                <span class="group-hover/korok:text-sky-400 transition duration-75 group-hover/korok:-translate-y-px delay-[225ms]" aria-hidden="true">e</span>
                                <span class="group-hover/korok:text-blue-400 transition duration-75 group-hover/korok:-translate-y-px delay-[250ms]" aria-hidden="true">e</span>
                                <span class="group-hover/korok:text-indigo-400 transition duration-75 group-hover/korok:-translate-y-px delay-[275ms]" aria-hidden="true">d</span>
                                <span class="group-hover/korok:text-violet-400 transition duration-75 group-hover/korok:-translate-y-px delay-[300ms]" aria-hidden="true">s</span>
                            </span>.
                        </p>
                    </div>
                </section>
                <section id="experience" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24">
                    <div class="sticky top-0 z-20 -mx-6 mb-4 w-screen bg-slate-900/75 px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0">
                        <h2 class="text-sm font-bold uppercase tracking-widest text-slate-200 lg:sr-only">Experience</h2>
                    </div>
                    <div>
                        <ol class="group/list">
                            <li class="mb-12">
                                <div class="group relative grid pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50">
                                    <div class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg"></div>
                                    <header class="z-10 mb-2 mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500 sm:col-span-2" aria-label="2024 to Present">2024 — Present</header>
                                    <div class="z-10 sm:col-span-6">
                                        <h3 class="font-medium leading-snug text-slate-200">
                                            <div>
                                                <a class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300  group/link text-base" href="https://www.klaviyo.com" target="_blank" rel="noreferrer noopener" aria-label="Senior Frontend Engineer, Accessibility at Klaviyo (opens in a new tab)">
                                                    <span class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"></span>
                                                    <span>Senior Frontend Engineer, Accessibility ·<!-- --> 
                                                        <span class="inline-block">Klaviyo<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:-translate-y-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px" aria-hidden="true"><path fill-rule="evenodd" d="M5.22 14.78a.75.75 0 001.06 0l7.22-7.22v5.69a.75.75 0 001.5 0v-7.5a.75.75 0 00-.75-.75h-7.5a.75.75 0 000 1.5h5.69l-7.22 7.22a.75.75 0 000 1.06z" clip-rule="evenodd"></path></svg>
                                                        </span>
                                                    </span>
                                                </a>
                                            </div>
                                        </h3>
                                        <p class="mt-2 text-sm leading-normal">Build and maintain critical components used to construct Klaviyo’s frontend, across the whole product. Work closely with cross-functional teams, including developers, designers, and product managers, to implement and advocate for best practices in web accessibility.</p>
                                        <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                                            <li class="mr-1.5 mt-2">
                                                <div class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300 ">JavaScript</div>
                                            </li>
                                            <li class="mr-1.5 mt-2">
                                                <div class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300 ">TypeScript</div>
                                            </li>
                                            <li class="mr-1.5 mt-2">
                                                <div class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300 ">React</div>
                                            </li>
                                            <li class="mr-1.5 mt-2">
                                                <div class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300 ">Storybook</div>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                            </li>
                        </ol>
                    </div>
                </section>
            </main>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            backgroundStyle: {
                background: 'radial-gradient(600px at 1000px 500px, rgba(29, 78, 216, 0.15), transparent 80%)' // กำหนดค่าเริ่มต้น
            }
        }
    },
    methods: {
        updateBackground(event) {
            const x = event.clientX;
            const y = event.clientY;

            // เปลี่ยนตำแหน่งของ radial-gradient ตามตำแหน่งเมาส์
            this.backgroundStyle.background = `radial-gradient(600px at ${x}px ${y}px, rgba(29, 78, 216, 0.15), transparent 80%)`;
        }
    }
}
</script>

<style lang="scss" scoped></style>
