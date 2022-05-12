<script>
    // direction -> column, row
    export let direction = "row";
</script>

<div class="box-group" style="flex-direction: {direction};">
    <slot />
</div>

<style>
    .box-group {
        display: flex;
        flex-wrap: wrap;
        align-content: flex-start;
        align-items: flex-start;
        justify-content: flex-start; 
    }
</style>
