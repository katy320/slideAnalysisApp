<template>
    <div class="AppBody">
        <Tabs @setPanel="setPanel" />
        <AnalyzePanel v-if="currentTab === 'AnalyzePanel'" />
        <ResultsPanel v-else />
        <ButtonsBar/>
    </div>
</template>

<script>
import Tabs from "@/components/Tabs"
import AnalyzePanel from "@/components/AnalyzePanel"
import ResultsPanel from "@/components/ResultsPanel"
import ButtonsBar from "@/components/ButtonsBar"

    export default {
        data() {
            return {
                buttonName: "analyze",
                currentTab: "AnalyzePanel"
            }
        },
        components: {
            Tabs,
            AnalyzePanel,
            ResultsPanel,
            ButtonsBar
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