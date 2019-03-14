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

