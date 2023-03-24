<script>
export default {
    data() {
        return {
            title: "-->Content goes Here<--"
        }
    }
}
</script>

<template>
    <div class="container">

        <div class="main-wrapper">
            <h1>{{ title }}</h1>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    width: 100%;
    height: 120px;
    background: rgb(28, 28, 28);
    color: white;

    display: flex;
    justify-content: center;

    .main-wrapper {
        width: 100%;
        max-width: 1200px;

        padding: 1em 0;
    }

}
</style>