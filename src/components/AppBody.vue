<!--This page deals with the entire desktop body area.
v-if & v-else are if/else statements controlling the view 
of the body area depending on which tab is clicked-->
<template>
    <div class="AppBody">
        <Tabs />
        <AnalyzePanel v-if="currentTab === 'AnalyzePanel'" />
        <ResultsPanel v-else />
        <ButtonsBar/>
    </div>
</template>

<!--import is to let this file know where the other related files are coming from.
export is where you write the components and data functions.-->
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

<!--This is where the CSS goes-->
<style scoped>
    .AppBody {
        background-color: var(--light-gray);
        padding-top: 30px;
        padding-bottom: 30px;
        font-size: 16px;
    }
</style>