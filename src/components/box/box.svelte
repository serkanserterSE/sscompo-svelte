<script>
    export let title = "",
        subtitle = "",
        iconUrl = "";
    export let width = "300px";
</script>

<div class="box" style="width: {width};">
    {#if title}
        <div class="box-head">
            <div>
                {#if iconUrl}
                    <div class="box-head-icon">
                        <img width="40" src={iconUrl} alt="ICON" />
                    </div>
                {/if}
            </div>
            <div>
                <div class="box-head-title">{title}</div>
                <div class="box-head-subtitle">{subtitle}</div>
            </div> 
        </div>
    {/if}
    <div class="box-content"><slot name="content" /></div>
    <div class="box-foot">
        <slot name="foot"></slot>
    </div>
</div>

<style>
    .box {
        margin: 5px;
        box-shadow: 2px 3px 9px 2px #00000041;
        padding: 5px;
        background-color: #fff;
        border-radius: 6px;
        min-width: 300px;
        max-width: 600px;
    }

    .box-head {
        padding: 5px;
        display: flex;
        flex-direction: row;
        align-items: center;
        align-content: space-around;
        justify-content: flex-start;
        border-bottom: 1px solid #00000041;
    }

    .box-head-title {
        font-size: 18px;
    }

    .box-head-icon {
        background-color: rgba(0, 0, 0, 0.2);
        border-color: rgba(0, 0, 0, 0.3);
        border-width: 1px;
        width: 50px;
        height: 50px;
        margin: 3px;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        align-content: center;
        flex-wrap: nowrap;
        flex-direction: row;
    }

    .box-head-subtitle {
        font-size: 14px;
        font-style: italic;
        color: rgba(0, 0, 0, 0.6);
    }

    .box-content {
        padding: 5px;
    }

    .box-foot { 
        border-top: 1px solid #00000041;
        padding: 5px;
    }
</style>
