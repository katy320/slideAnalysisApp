<template>
    <div class="AnalyzeButton">
        <button>Analyze</button>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    button {
        --height: 40px;
        height: var(--height);
        width: 100px;
        border: none;
        border-radius: calc( var(--height) / 2 );
        background-color: var(--blue);
        color: white;
        box-shadow: 0px 1px 7px -1px;
        outline: none;
    }

</style>
