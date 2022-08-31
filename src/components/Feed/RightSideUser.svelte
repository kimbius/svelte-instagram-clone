<div class="p-5 flex flex-col gap-4">
    <div class="flex justify-between items-center">
        <div class="flex gap-3 items-center">
            <div class="h-[55px] w-[55px] bg-gray-200 rounded-full" />
            <div>
                <h1 class="font-bold">kimbiusss</h1>
                <p class="text-gray-500 text-sm">ขลุ่ย</p>
            </div>
        </div>
        <h2 class="text-blue-500 font-bold text-sm">เปลี่ยน</h2>
    </div>
    <div class="flex flex-col gap-3">
        <div class="flex justify-between">
            <h2 class="text-gray-500 font-bold text-sm">แนะนำสำหรับคุณ</h2>
            <h2 class="text-gray-800 font-bold text-sm">ดูทั้งหมด</h2>
        </div>
        {#each Array(5) as _, i}
            <div class="flex justify-between items-center">
                <div class="flex gap-3 items-center">
                    <div class="h-[35px] w-[35px] bg-gray-200 rounded-full" />
                    <div>
                        <h1 class="font-bold text-sm">kimbiusss</h1>
                        <p class="text-gray-500 text-xs">
                            ติดตามโดย kimbiuss + อีก 1 คน
                        </p>
                    </div>
                </div>
                <h2 class="text-blue-500 font-bold text-sm">ติดตาม</h2>
            </div>
        {/each}
    </div>
    <footer class="text-sm text-gray-400 mt-5">
        <p>© 2022 INSTAGRAM FROM META</p>
        <a href="https://github.com/kimbius/svelte-instagram-clone" target="_">
            <img
                src="https://img.shields.io/badge/GitHub-source%20code-lightgrey"
                alt=""
            />
        </a>
    </footer>
</div>
