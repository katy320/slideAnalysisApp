<template>
    <div class="AnalyzePanel">
        <img src = "@/assets/image.png" height =100px width=100px/>
        <br>
        <button> Add Images </button>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .AnalyzePanel {
        background-color: white;
        height: 400px;
        width: var(--panelWidth);
        margin-top: 30px;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 30px;
        border-radius: 3px;
        box-shadow: 0px 1px 7px -1px;
    }
    button {
        --height: 40px;
        height: var(--height);
        width: 100px;
        border: none;
        border-radius: calc( var(--height) / 2 );
        background-color: white;
        color: var(--blue);
        box-shadow: 0px 1px 7px -1px;
        outline: none;
    }
    img {
        margin-top: 50px;
    }
</style>