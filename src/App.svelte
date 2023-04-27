<script>
    import { loggedIn as loggedInStore } from "./lib/store";
    import LoginModal from "./lib/LoginModal.svelte";
    import LogoutButton from "./lib/LogoutButton.svelte";

    let loggedInBool;
    loggedInStore.subscribe((loggedIn) => {
        loggedInBool = loggedIn;
    });
</script>

<main class="grid place-items-center w-screen h-screen">
    <!-- Login Modal if not Logged In -->
    {#if !loggedInBool}
        <LoginModal />
    {:else}
        <div>
            <LogoutButton />
        </div>
    {/if}
</main>

<style global lang="postcss">
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>
