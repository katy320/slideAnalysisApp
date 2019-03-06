<template>
    <div class="AppBody">
        <Tabs @setPanel="setPanel" />
        <ImagePanel v-if="currentTab === 'ImagePanel'" />
        <SavedPanel v-else />
        <AnalyzeButton/>
    </div>
</template>

<script>
import Tabs from "@/components/Tabs"
import AnalyzeButton from "@/components/AnalyzeButton"
import ImagePanel from "@/components/ImagePanel"
import SavedPanel from "@/components/SavedPanel"

    export default {
        data() {
            return {
                buttonName: "analyze",
                currentTab: "ImagePanel"
            }
        },
        components: {
            Tabs,
            AnalyzeButton,
            ImagePanel,
            SavedPanel
        },
        methods: {
            setPanel(event) {
                this.currentTab = event
            }
        }
    }
    
</script>

<style scoped>
    .AppBody {
        background-color: var(--light-gray);
        padding-top: 30px;
        padding-bottom: 30px;
        font-size: 16px;
    }
</style>