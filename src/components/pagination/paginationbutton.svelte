<script>
    import { createEventDispatcher } from "svelte";
    export let pageIndex = 0;
    export let style = "";
    const dispatch = createEventDispatcher();
    const pgclick = () => {
        dispatch("pgbuttonclick", {
            index: pageIndex,
        });
    };
</script>

{#if style}
    <span {style} on:click={pgclick}>{pageIndex}</span>
{:else}
    <span class="pg-button" on:click={pgclick}>{pageIndex}</span>
{/if}

<style>
    .pg-button {
        margin: 3px;
        padding: 3px; 
        cursor: pointer;
        border-radius: 16px;
        box-shadow: 1px 1px 1px 2px rgba(0, 0, 0, 0.4);
        height: 20px;
        width: 20px;
        display: flex;
        align-items: center;
        flex-direction: row;
        flex-wrap: nowrap;
        align-content: center;
        justify-content: center;
        align-items: center;
    }

    .pg-button:hover {
        box-shadow: 1px 1px 2px 3px rgba(0, 0, 0, 0.4);
    }

    .pg-button:active {
        box-shadow: inset 0.7px 0.7px 1px 2px rgba(0, 0, 0, 0.4);
    }
</style>
