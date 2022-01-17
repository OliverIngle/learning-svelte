<script lang="ts">
    import Toggle from "./Toggle.svelte";

    export let title;

    let onDisplay: boolean;

</script>

<section>
    <h1 class="title">{title}</h1>

    <Toggle bind:on={onDisplay} />

    {#if onDisplay}
        <slot></slot>
    {/if}
</section>

<style>
    h1.title {
        margin-bottom: 1rem;
        font-size: 2rem;
        font-weight: bold;
    }

    section {
        margin: 1rem;
        padding: 1rem;
        border-radius: 20px;
        box-shadow: 0 3px 10px darkgrey;
    }
</style>