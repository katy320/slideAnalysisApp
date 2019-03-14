<!--This is where you edit each result row's output view and functionality.
You have to edit the eyeIcon pop up here.-->
<template>
    <div class="ResultRow">

        <div class="index">Number</div>
        <div class="filename">Name</div>
        <div class="count">Count</div>

        <div class="eyebtn">
            <fa-icon icon="eye" @click="onImagePopup"/>
        </div>
     
    </div>
</template>

<!--import is to let this file know where the other related files are coming from.
export is where you write the methods and other functionalities-->
<script>
import EventBus from "@/EventBus.js"

export default {
    methods: {
        onImagePopup() {
            EventBus.$emit("onImagePopup")
        }
    }
}
</script>

<!--This is where the CSS goes-->
<style scoped>

    td {
        border: 1px solid #cccccc;
    }
    
    .ResultRow {
        display: grid;
        grid-template-columns: 60fr 250fr 250fr 140fr;
        margin-left: 30px;
        margin-right: 30px;
        margin-top: 10px;
        margin-bottom: 10px;
        border-bottom: 1px solid var(--light-gray);
    }

    .eyebtn {
        cursor: pointer;
    }

</style>
