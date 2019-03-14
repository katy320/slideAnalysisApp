<!--This page is for the Analyze/Results Tab functionalties & styles.
@click is onclick.
:class is binding a class to manipulate an element’s class list and its inline styles.-->
<template>
    <div class="Tabs">
       <div
        @click="activateAnalyze"
        class="TabButton"
        :class="{isActive: activeTab === 'analyze' }">
        Analyze
        </div>

       <div
        @click="activateSaved"
        class="TabButton"
        :class="{isActive: activeTab === 'saved' }">
        Results
        </div>
    </div>
</template>

<!--import is to let this file know where the other related files are coming from.
export is where you write the data functions and methods.-->
<script>
import EventBus from "@/EventBus.js"

export default {
    data() {
        return {
            activeTab: "analyze"
        }
    },
    methods: {
        activateAnalyze() {
            this.activeTab = "analyze"
            EventBus.$emit("setPanel", "AnalyzePanel")
        },
        activateSaved() {
            this.activeTab = "saved"
            EventBus.$emit("setPanel", "ResultsPanel")
        }
    }
}
</script>

<!--here is where the CSS goes-->
<style scoped>
    .Tabs {
        height: 50px;
        width: var(--panelWidth);
        border-radius: 3px;
        background-color: white;
        font-size: 16px;
        text-align: center;
        display: grid;
        grid-template-columns: 1fr 1fr;
        cursor: pointer;
        margin-left: auto;
        margin-right: auto;
    }

    .TabButton {
        line-height: 50px;
        box-shadow: 0px 1px 7px -1px;
        border-radius: 3px;
    }

    .isActive {
        border-bottom: 3px solid var(--blue);
    }

</style>
