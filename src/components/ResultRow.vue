<template>
    <div class="ResultRow">

        <div class="index">Index Number</div>
        <div class="filename">File Name</div>
        <div class="count">Eosinophil Count</div>

        <div class="eyebtn">
            <fa-icon icon="eye" />
        </div>
     
    </div>
</template>
<script>
export default {
    
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

</style>

