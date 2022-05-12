<script>
    import Box from "../box/box.svelte";

    export let title = "",
        subtitle = "",
        iconUrl = "";
    export let isOpen = false;
</script>

<div class="modal" style="display:{isOpen ? 'block' : 'none'};">
    <div class="modal-content slide-in">
        <Box {title} {subtitle} {iconUrl} width="100%">
            <div slot="content"><slot name="content" /></div>
            <div slot="foot">
                <div class="footer">
                    <div><slot name="custom-buttons" /></div>
                    <div>
                        <button
                            type="button"
                            on:click={() => {
                                isOpen = !isOpen;
                            }}>Kapat</button
                        >
                    </div>
                </div>
            </div>
        </Box>
    </div>
</div>

<style>
    .modal {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        z-index: 99999;
        background-color: rgba(0, 0, 0, 0.4);
    }

    .modal-content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .footer {
        display: flex;
        flex-direction: row;
        align-items: center;
        flex-wrap: nowrap;
        align-content: center;
        justify-content: space-between;
    }

    .slide-in {
        animation: slide-in 0.7s
            cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
    }
    @keyframes slide-in {
        0% {
            transform: translate(-50%, -650%) rotateX(-30deg) scale(0);
            opacity: 0;
        }
        100% {
            transform: translate(-50%, -50%) rotateX(0) scale(1);
            opacity: 1;
        }
    }
</style>
