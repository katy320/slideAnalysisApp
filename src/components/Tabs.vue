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
        Saved Slides
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            activeTab: "analyze"
        }
    },
    methods: {
        activateAnalyze() {
            this.activeTab = "analyze"
            this.$emit("setPanel", "ImagePanel")
        },
        activateSaved() {
            this.activeTab = "saved"
            this.$emit("setPanel", "SavedPanel")
        }
    }
}
</script>

<style scoped>
    .Tabs {
        height: 50px;
        width: var(--panelWidth);
        border-radius: 3px;
        background-color: var(--blue);
        font-size: 16px;
        text-align: center;
        display: grid;
        grid-template-columns: 1fr 1fr;
        cursor: pointer;
        margin-left: auto;
        margin-right: auto;
    }


    .TabButton {
        height: 50px;
        background-color: white;
        height: 100%;
        box-shadow: 0px 1px 7px -1px;
        border-radius: 3px;
    }

    .isActive {
        height: 90%;
    }

</style>
