<script>
    import { loggedIn } from "./store";

    function LogOut() {
        loggedIn.update(_ => false);
    }
</script>

<button class="btn" on:click={LogOut}>Log Out</button>