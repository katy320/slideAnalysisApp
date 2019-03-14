<!--This is the home landing screen for the desktop app.
It contains the image icon and (Add Image) button inside the body if the screen is empty.<style scoped>
It contains a progress bar if images are being uploaded, 
and the (Add Image) button will be moved to the button bar area below.
</style>

-->
</style>
<template>
    <div class="AnalyzePanel">
        <img src = "@/assets/image.png" height =100px width=100px/>
        <br>
        <button> Add Images </button>
    </div>
</template>

<!--This is where functionalities for the Analyze tab goes.-->
<script>
    export default {}
</script>

<!--This is where the CSS goes-->
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