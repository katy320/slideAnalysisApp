<template>
    <div class="ImageModal background" @click="onPopupClose">
        <div class="body">
            Image Not Found
        </div>
    </div>
</template>

<script>
export default {
    methods:  {
        onPopupClose() {
            this.$emit("onPopupClose")
        }
    }
}
</script>

<style scoped>
    .ImageModal {
        position: fixed;
        width: 100vw;
        height: 100vh;
        top: 0;
        left: 0;
        display: grid;
        align-items: center;
        justify-content: center;
    }

    .background {
        background: rgba(0, 0, 0, 0.7);
    }

    .body {
        position: relative;
        width: 300px;
        height: 50vh;
        background-color: white;
        border-radius: 5px;
        overflow: hidden;
    }

</style>
