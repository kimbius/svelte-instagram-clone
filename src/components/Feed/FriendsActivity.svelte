<div class="bg-white border rounded-lg p-5 overflow-hidden flex gap-6">
    {#each Array(3) as _, i}
        <div class="flex flex-col items-center gap-2">
            <div
                class="relative rounded-full h-[65px] w-[65px] bg-gradient-to-tr from-yellow-400 via-red-600 to-purple-700"
            >
                <div
                    class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 w-[55px] h-[55px] bg-gray-100 rounded-full ring-white ring-[3px]"
                />
                <div
                    class="absolute py-[.1rem] px-[.3rem] rounded bg-rose-500 text-white text-[.5rem] -bottom-1 left-1/2 -translate-x-1/2"
                >
                    Live
                </div>
            </div>
            <h1 class="text-xs">kimbiusss</h1>
        </div>
    {/each}
</div>
