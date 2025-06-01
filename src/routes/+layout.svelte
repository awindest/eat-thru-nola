<script>
	let { children } = $props();
</script>

{@render children?.()}

<style>
    @font-face {
        font-family: 'TamaraElainaDemoRegular';
        src: url('/fonts/TamaraElainaDemoRegular.ttf');
        font-style: normal;
        font-weight: 500;
        font-display: swap;
    }
    :global(body) {
        font-family: 'TamaraElainaDemoRegular', san-serif;
    }
</style>