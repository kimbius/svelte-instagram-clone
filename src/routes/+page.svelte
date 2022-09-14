<script>
    import FriendsActivity from "../components/Feed/FriendsActivity.svelte";
    import PostsFeed from "../components/Feed/PostsFeed.svelte";
    import RightSideUser from "../components/Feed/RightSideUser.svelte";
</script>

<div class="container my-5">
    <div class="grid grid-cols-10 gap-3">
        <div class="flex justify-end md:col-span-7 col-span-10">
            <div class="flex flex-col gap-2 w-full md:max-w-[500px]">
                <FriendsActivity />
                <PostsFeed />
            </div>
        </div>
        <div class="hidden md:block col-span-3">
            <RightSideUser />
        </div>
    </div>
</div>
