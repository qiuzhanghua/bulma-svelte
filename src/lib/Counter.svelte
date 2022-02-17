<script>
    let count = 0
    const increment = () => {
        count += 1
    }
</script>
<!--<svelte:head>-->
<!--    <link rel="stylesheet" href="css/default.css">-->
<!--</svelte:head>-->
<button class="button is-primary is-responsive is-outlined is-rounded" on:click={increment}>
    Clicks: {count}
</button>

<style lang="scss">
    @import "../style/default.sass";
</style>
