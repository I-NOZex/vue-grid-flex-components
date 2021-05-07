<template>
    <div class="cell-container">
        <slot />
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.cell-container {
    flex: 1 0 0;
    align-self: auto;
    display: inline-flex;
    justify-content: center;
    margin: 15px;
    padding: 20px;
}
</style>