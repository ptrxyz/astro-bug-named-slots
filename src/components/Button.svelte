<div on:click={console.log}>
    <slot />
</div>

<style>
    div {
        background-color: red;
        user-select: none;
        padding: 10px;
        display: inline-block;
        cursor: pointer;
        border-radius: 10px;
    }
</style>
