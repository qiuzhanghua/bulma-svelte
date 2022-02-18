<script>
    let modelOpened = false
    $: opened = modelOpened ? "is-active" : ""

    function dialog() {
        modelOpened = !modelOpened
    }
</script>

<svelte:head>
    <link rel="stylesheet" href="css/bulma.min.css">
</svelte:head>

<section class="section">
    <button class="button is-primary is-outlined" on:click={dialog}>Open Dialog</button>
    <div class="container">
        <h1 class="title">
            Hello World
        </h1>
        <p class="subtitle">
            My first website with <strong>Bulma</strong>!
        </p>
    </div>
</section>

<div class="modal {opened}">
    <div class="modal-background"></div>
    <div class="modal-card">
        <header class="modal-card-head">
            <p class="modal-card-title">Modal title</p>
            <button class="delete" aria-label="close" on:click={dialog}></button>
        </header>
        <section class="modal-card-body">
            Hello, I am a Dialog!
        </section>
        <footer class="modal-card-foot">
            <button class="button is-success">Save changes</button>
            <button class="button" on:click={dialog}>Cancel</button>
        </footer>
    </div>
</div>
