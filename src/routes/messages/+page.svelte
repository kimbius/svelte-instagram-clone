<script>
    let select_chat = "";

    let chat_items = [
        {
            isSender: false,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: false,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: false,
            content: "Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet.",
        },
        {
            isSender: false,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
        {
            isSender: true,
            content: "Lorem ipsum dolor sit amet.",
        },
    ];
</script>

<div class="container my-5">
    <div class="bg-white border rounded-lg">
        <div class="grid grid-cols-10 min-h-[50vh]">
            {#if !select_chat}
                <div class="col-span-10 md:col-span-3 flex flex-col border-r">
                    <div class="flex border-b justify-center p-4">
                        <h1 class="font-bold text-lg">kimbiusss</h1>
                    </div>
                    <div class="flex flex-col">
                        <div class="flex justify-between px-4 py-2">
                            <h1 class="font-bold text-lg">ข้อความ</h1>
                            <p class="text-blue-500 font-bold">
                                ความคิดเห็น 1 รายการ
                            </p>
                        </div>
                        <div class="flex flex-col pb-2">
                            {#each Array(5) as _, i}
                                <div
                                    on:click={() =>
                                        (select_chat = i.toString())}
                                    class="px-4 py-2 hover:bg-gray-100 active:bg-gray-200"
                                >
                                    <div class="flex gap-3 items-center">
                                        <div
                                            class="relative border border-1 border-gray-300 h-[55px] w-[55px] bg-gray-200 rounded-full"
                                        >
                                            <div
                                                class="absolute bottom-0 right-0 h-[15px] w-[15px] ring-3 ring-white bg-green-300 rounded-full"
                                            />
                                        </div>
                                        <div>
                                            <h1 class="font-bold text-base">
                                                kimbiusss
                                            </h1>
                                            <p class="text-gray-500 text-sm">
                                                กำลังใช้งาน
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            {/each}
                        </div>
                    </div>
                </div>
            {:else}
                <div class="col-span-10">
                    <div class="border-b px-4 py-3">
                        <div class="flex justify-between">
                            <div class="flex gap-3 items-center">
                                <button on:click={() => (select_chat = "")}>
                                    <svg
                                        xmlns="http://www.w3.org/2000/svg"
                                        width="16"
                                        height="16"
                                        fill="currentColor"
                                        class="bi bi-chevron-left"
                                        viewBox="0 0 16 16"
                                    >
                                        <path
                                            fill-rule="evenodd"
                                            d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"
                                        />
                                    </svg>
                                </button>
                                <div class="flex gap-3 items-center">
                                    <div
                                        class="relative h-[35px] w-[35px] bg-gray-200 rounded-full"
                                    >
                                        <div
                                            class="absolute bottom-0 right-0 h-[10px] w-[10px] ring-3 ring-white bg-green-300 rounded-full"
                                        />
                                    </div>
                                    <div>
                                        <h1 class="font-bold text-sm">
                                            kimbiusss
                                        </h1>
                                        <p class="text-gray-500 text-xs">
                                            กำลังใช้งาน
                                        </p>
                                    </div>
                                </div>
                            </div>
                            <button>
                                <svg
                                    aria-label="ดูรายละเอียดของการสนทนา"
                                    class="_ab6-"
                                    color="#262626"
                                    fill="#262626"
                                    height="24"
                                    role="img"
                                    viewBox="0 0 24 24"
                                    width="24"
                                    ><circle
                                        cx="12.001"
                                        cy="12.005"
                                        fill="none"
                                        r="10.5"
                                        stroke="currentColor"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                    /><circle
                                        cx="11.819"
                                        cy="7.709"
                                        r="1.25"
                                    /><line
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        x1="10.569"
                                        x2="13.432"
                                        y1="16.777"
                                        y2="16.777"
                                    /><polyline
                                        fill="none"
                                        points="10.569 11.05 12 11.05 12 16.777"
                                        stroke="currentColor"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                    /></svg
                                >
                            </button>
                        </div>
                    </div>
                    <div class="relative h-[50vh] overflow-y-auto">
                        <div class="flex flex-col gap-3 p-5">
                            {#each chat_items as Item}
                                <div
                                    class="flex gap-3"
                                    class:flex-row-reverse={Item.isSender}
                                >
                                    <div
                                        class="relative h-[35px] w-[35px] bg-gray-200 rounded-full"
                                    />
                                    <div
                                        class="max-w-xs p-2 px-3 text-base rounded-2xl ring-1 ring-gray-200"
                                    >
                                        <p>{Item.content}</p>
                                    </div>
                                </div>
                            {/each}
                        </div>
                    </div>
                    <div class="p-5">
                        <div
                            class="bg-white rounded-full border py-3 px-5 flex justify-between items-center w-full"
                        >
                            <div class="flex items-center gap-4">
                                <svg
                                    aria-label="อีโมจิ"
                                    class="_ab6-"
                                    color="#262626"
                                    fill="#262626"
                                    height="24"
                                    role="img"
                                    viewBox="0 0 24 24"
                                    width="24"
                                    ><path
                                        d="M15.83 10.997a1.167 1.167 0 101.167 1.167 1.167 1.167 0 00-1.167-1.167zm-6.5 1.167a1.167 1.167 0 10-1.166 1.167 1.167 1.167 0 001.166-1.167zm5.163 3.24a3.406 3.406 0 01-4.982.007 1 1 0 10-1.557 1.256 5.397 5.397 0 008.09 0 1 1 0 00-1.55-1.263zM12 .503a11.5 11.5 0 1011.5 11.5A11.513 11.513 0 0012 .503zm0 21a9.5 9.5 0 119.5-9.5 9.51 9.51 0 01-9.5 9.5z"
                                    /></svg
                                >
                                <p class="text-gray-400">ส่งข้อความ...</p>
                            </div>
                            <div class="flex gap-3">
                                <svg
                                    aria-label="เพิ่มรูปภาพหรือวิดีโอ"
                                    class="_ab6-"
                                    color="#262626"
                                    fill="#262626"
                                    height="24"
                                    role="img"
                                    viewBox="0 0 24 24"
                                    width="24"
                                    ><path
                                        d="M6.549 5.013A1.557 1.557 0 108.106 6.57a1.557 1.557 0 00-1.557-1.557z"
                                        fill-rule="evenodd"
                                    /><path
                                        d="M2 18.605l3.901-3.9a.908.908 0 011.284 0l2.807 2.806a.908.908 0 001.283 0l5.534-5.534a.908.908 0 011.283 0l3.905 3.905"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                    /><path
                                        d="M18.44 2.004A3.56 3.56 0 0122 5.564h0v12.873a3.56 3.56 0 01-3.56 3.56H5.568a3.56 3.56 0 01-3.56-3.56V5.563a3.56 3.56 0 013.56-3.56z"
                                        fill="none"
                                        stroke="currentColor"
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                    /></svg
                                >
                                <svg
                                    aria-label="ถูกใจ"
                                    class="_ab6-"
                                    color="#262626"
                                    fill="#262626"
                                    height="24"
                                    role="img"
                                    viewBox="0 0 24 24"
                                    width="24"
                                    ><path
                                        d="M16.792 3.904A4.989 4.989 0 0121.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 014.708-5.218 4.21 4.21 0 013.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 013.679-1.938m0-2a6.04 6.04 0 00-4.797 2.127 6.052 6.052 0 00-4.787-2.127A6.985 6.985 0 00.5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 003.518 3.018 2 2 0 002.174 0 45.263 45.263 0 003.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 00-6.708-7.218z"
                                    /></svg
                                >
                            </div>
                        </div>
                    </div>
                </div>
            {/if}
        </div>
    </div>
</div>
