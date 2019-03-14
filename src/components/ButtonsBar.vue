<template>
    <div class="ButtonsBar">
        <span>left stuff</span>
        <span>
            <button class="addimagesbtn" v-if="currentTab === 'AnalyzePanel'">Add Images</button>
            <button v-if="currentTab === 'AnalyzePanel'">Analyze</button>
            <button v-else>Done</button>
        </span>
    </div>
</template>

<script>
import EventBus from "@/EventBus.js"

export default {
    data() {
        return {
            currentTab: "AnalyzePanel"
        }
    },
    created() {
        EventBus.$on("setPanel", event => this.currentTab = event )
    }    
}
</script>

<style scoped>
   .ButtonsBar {
        height: 50px;
        width: var(--panelWidth);
        border-radius: 3px;
        font-size: 16px;
        text-align: center;
        display: grid;
        grid-template-columns: 1fr 1fr;
        cursor: pointer;
        margin-left: auto;
        margin-right: auto;
   }
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
    .addimagesbtn {
        width: 120px;
        color: var(--blue);
        background-color: white;
    }
</style>
