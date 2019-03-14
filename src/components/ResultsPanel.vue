<!--This page is for writing the functionalities behind viewing the Results 
when the backend completes analyzing the images.
v-for is a loop function-->
<template>
    <div class="ResultsPanel">
        <div class="tableHeaders">
            <span>Index</span>
            <span>File Name</span>
            <span>Eosinophil Count</span>
            <span>High Power Field</span>
        </div>
        <ul>
            <li v-for="row in rows" :key="row">
                <ResultRow />
            </li>
        </ul>
    </div>
</template>

<!--import is to let this file know where the other related files are coming from.
export is where you write the components and data functions.-->
<script>
import ResultRow from "@/components/ResultRow"

export default {
    components: {
        ResultRow
    },
    data() {
        return {
            rows: [1,2,3,4,5,6,7,8,9,10]
        }
    }
}
</script>

<!--This is where the CSS goes-->
<style scoped>
    .ResultsPanel {
        background-color: white;
        height: 400px;
        width: var(--panelWidth);
        margin-top: 30px;
        margin-left: auto;
        margin-right: auto;
        margin-bottom: 30px;
        border-radius: 3px;
        box-shadow: 0px 1px 7px -1px;
        overflow-y: scroll;
    }
    .tableHeaders {
        display: grid;
        grid-template-columns: 60fr 250fr 250fr 140fr;
        margin-left: 30px;
        margin-right: 30px;
        margin-top: 30px;
        height: 30px;
        border-bottom: 1px solid var(--light-gray);
        font-weight: bold;
    }
    ul {
        list-style: none;
        padding-left: 0%;
    }
    .ResultsPanel::-webkit-scrollbar-thumb {
        background-color: blue;
    }
</style>
