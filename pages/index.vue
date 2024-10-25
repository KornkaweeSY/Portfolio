<template>
    <div 
        class="max-w-full h-screen bg-slate-900 leading-relaxed text-slate-400 antialiased selection:bg-teal-300 selection:text-teal-900"
        @mousemove="updateBackground" ref="backgroundDiv">
        <div
            class="pointer-events-none fixed inset-0 z-30 transition duration-300 lg:absolute"
            :style="backgroundStyle"
        ></div>
        <div class="flex justify-between">
            <header class="w-1/2">
                <div>
                    <h1 class="text-slate-200 text-4xl font-bold">Kornkawee Songyen</h1>
                    <h2 class="text-slate-200 text-lg font-semibold">Software Engineer</h2>
                    <p class="text-slate-200 text-sm">Lorem ipsum dolor sit amet consectetur adipisicing elit. In temporibus laboriosam consequuntur pariatur reiciendis quia consectetur obcaecati! Similique atque non illo explicabo eligendi tempore. Magni accusamus laborum distinctio vel autem.</p>
                </div>
            </header>
            <div class="w-1/2">
                <div>
                    <h1></h1>
                </div>
            </div>
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
