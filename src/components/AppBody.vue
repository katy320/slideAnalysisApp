<template>
    <div class="AppBody">
        <Tabs />
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
import EventBus from "@/EventBus.js"

    export default {
        data() {
            return {
                currentTab: "AnalyzePanel"
            }
        },
        components: {
            Tabs,
            AnalyzePanel,
            ResultsPanel,
            ButtonsBar
        },
        created() {
            EventBus.$on("setPanel", event => this.currentTab = event )
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