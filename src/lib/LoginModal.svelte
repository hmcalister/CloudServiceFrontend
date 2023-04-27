<script>
    import { loggedIn } from "./store.js";

    function LogIn() {
        loggedIn.update((_) => true);
    }
</script>

<label for="LogIn-Modal" class="btn">Log In</label>

<input type="checkbox" id="LogIn-Modal" class="modal-toggle" />
<label for="LogIn-Modal" class="modal cursor-pointer">
    <label class="modal-box relative">
        <h3>Log In</h3>
        <p class="py-4">Some Login Text</p>
        <div class="modal-action">
            <button class="btn" on:click={LogIn}>Log In</button>
        </div>
    </label>
</label>
