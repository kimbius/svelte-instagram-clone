<script>
    import BIcon from "./BIcon.svelte";
</script>

<nav class="h-[60px] border-b-[1px] p-3 bg-white">
    <div
        class="container grid grid-cols-3 justify-between items-center h-full w-full"
    >
        <div>
            <a href="/">
                <BIcon Icon="Instagram" height="29" width="103" viewBox="32 4 113 32"/>

            </a>
        </div>
        <div>
            <input
                type="text"
                placeholder="ค้นหา"
                class="bg-gray-200/50 rounded-lg p-2 px-4 w-full"
            />
        </div>
        <div class="flex items-center gap-5 justify-self-end">
            <a href="/">
                <BIcon Icon="Home" />
            </a>
            <a href="/messages">
                <BIcon Icon="Message" />
            </a>
            <button>
                <BIcon Icon="NewPost" />
            </button>
            <a href="/explore">
                <BIcon Icon="Explore" />
            </a>
            <a href="/account/activity">
                <BIcon Icon="Activity" />
            </a>
        </div>
    </div>
</nav>
