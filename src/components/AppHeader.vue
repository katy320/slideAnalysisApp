<!--This page holds the header which contains the project icon, the title "Digital Pathology" 
and the EXIT button to close the desktop app.-->
<template>
    <div class="AppHeader">
        <img src="@/assets/logo.png" width=69px height=69px/>
        <h1> Digital Pathology </h1>
        <button> Exit </button>
    </div>
</template>

<!--This is where functionalities for the header area goes.-->
<script>
    export default {}

</script>

<!--This is where the CSS goes-->
<style scoped>
    .AppHeader { 
        background-color: var(--blue);
        height: 100px;
        display: grid;
        grid-template-columns: 100px auto 100px;
    }
    img {
        height: 69px;
        width: 69px;
        align-self: center;
    }
    button {
        --height: 40px;
        height: var(--height);
        width: 84px;
        border: none;
        border-radius: calc( var(--height) / 2 );
        background-color: white;
        box-shadow: 0px 1px 7px -1px;
        outline: none;
    }
    h1{
        display: grid;
        font-size: 30px;
        text-align: left;
        vertical-align: bottom;
        align-content: flex-end;
        color: white;
    }
</style>