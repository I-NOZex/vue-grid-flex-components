<template>
    <div class="row-container">
        <slot />
    </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.row-container {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: flex-start;
    align-content: stretch;
    align-items: stretch;
    padding: 0 15px;
}
</style>