<script>
    import FriendsActivity from "../components/Feed/FriendsActivity.svelte";
    import PostsFeed from "../components/Feed/PostsFeed.svelte";
    import RightSideUser from "../components/Feed/RightSideUser.svelte";
</script>

<div class="container my-5">
    <div class="grid grid-cols-10 gap-3">
        <div class="col-span-6">
            <div class="flex flex-col gap-5">
                <FriendsActivity />
                <PostsFeed />
            </div>
        </div>
        <div class="col-span-4">
            <RightSideUser />
        </div>
    </div>
</div>
