<template>
    <div class="grid-container" :style="cssVars">
        <slot />
    </div>
</template>

<script>
export default {
    props: {
        rows: {
            type: Number,
            default: 1
        },
        columns: {
            type: Number,
            default: 1
        },
        rowGap: {
            type: Number,
            default: 15
        },
        columnGap: {
            type: Number,
            default: 15
        }        
    },

    computed: {
        cssVars() {
            return {
                '--grid-columns': `repeat(${this.columns}, 1fr)`,
                '--grid-rows': `repeat(${this.rows}, 1fr)`,
                '--column-gap': `${this.columnGap}px`,
                '--row-gap': `${this.rowGap}px`,
            };
        }
    }
};
</script>

<style lang="scss" scoped>
.grid-container {
    display: grid;
    grid-template-columns: var(--grid-columns);
    grid-template-rows: var(--grid-rows);
    grid-column-gap: var(--column-gap);
    grid-row-gap: var(--row-gap);
}

@media screen and (max-width: 768px) {
    .grid-container {
        --grid-columns:repeat(1, 1fr) !important; 
    }
}
</style>