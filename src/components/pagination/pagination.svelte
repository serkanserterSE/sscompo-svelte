<script>
    import Paginationbutton from "./paginationbutton.svelte";
    export let pageCount = -1;
    let nums = [...Array(pageCount).keys()];
</script>

<div class="pg">
    {#each nums as num}
        <Paginationbutton
            pageIndex={num + 1}
            on:pgbuttonclick={(event) => {
                let index = event.detail.index;
            }}
        />
    {/each}
</div>

<style>
    .pg {
        display: flex;
        flex-direction: row;
    }
</style>
