<template>
    <div id="app">
        <div class="grid-example">
            <h1>Grid Example</h1>
            <GridLayout :rows="2" :columns="4">
                <div class="grid-cell-item">Row 1 - Col 1</div>
                <div class="grid-cell-item">Row 1 - Col 2</div>
                <div class="grid-cell-item">Row 1 - Col 3</div>
                <div class="grid-cell-item">Row 1 - Col 4</div>

                <div class="grid-cell-item">Row 2 - Col 1</div>
                <div class="grid-cell-item">Row 2 - Col 2</div>
                <div class="grid-cell-item">Row 2 - Col 3</div>
                <div class="grid-cell-item">Row 2 - Col 4</div>
            </GridLayout>
        </div>

        <div class="flexbox-example">
            <h1>Row/Cell Flexbox Example</h1>
            <Row>
                <Cell>
                    <p>Flex cell left</p>
                </Cell>
                <Cell>
                    <p>Flex cell middle</p>
                </Cell>
                <Cell>
                    <p>Flex cell right</p>
                </Cell>
            </Row>
        </div>

        <div class="grid-flexbox-example">
            <h1>Grid with Flexbox Childen Example</h1>
            <GridLayout :rows="2" :columns="2">
                <Row>
                    <Cell>
                        <p>Row 1 - Col 1 - Flex cell left</p>
                    </Cell>
                    <Cell>
                        <p>Row 1 - Col 1 - Flex cell middle</p>
                    </Cell>
                    <Cell>
                        <p>Row 1 - Col 1 - Flex cell right</p>
                    </Cell>
                </Row>

                <Row>
                    <Cell>
                        <p>Row 1 - Col 2 - Flex cell left</p>
                    </Cell>
                    <Cell>
                        <p>Row 1 - Col 2 - Flex cell middle</p>
                    </Cell>
                    <Cell>
                        <p>Row 1 - Col 2 - Flex cell right</p>
                    </Cell>
                </Row>

                <Row>
                    <Cell>
                        <p>Row 2 - Col 1 - Flex cell left</p>
                    </Cell>
                    <Cell>
                        <p>Row 2 - Col 1 - Flex cell middle</p>
                    </Cell>
                    <Cell>
                        <p>Row 2 - Col 1 - Flex cell right</p>
                    </Cell>
                </Row>

                <Row>
                    <Cell>
                        <p>Row 2 - Col 2 - Flex cell left</p>
                    </Cell>
                    <Cell>
                        <p>Row 2 - Col 2 - Flex cell middle</p>
                    </Cell>
                    <Cell>
                        <p>Row 2 - Col 2 - Flex cell right</p>
                    </Cell>
                </Row>                                                
            </GridLayout>
        </div>        
    </div>
</template>

<script>
import GridLayout from "@/components/CssGrid.vue";
import Row from "@/components/FlexRow.vue";
import Cell from "@/components/FlexCell.vue";

export default {
    name: "App",
    components: {
        GridLayout,
        Row,
        Cell
    }
};
</script>

<style lang="scss">
body {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    background-color: #41b883;
    color: #ffffff;
    margin: 0;
}

#app {
    margin: 20px;
}

.grid-example,
.flexbox-example,
.grid-flexbox-example {
    margin: 40px 0;
}

.grid-cell-item {
    background-color: rgba(12, 118, 224, 0.1);
    padding: 10px;
}

.row-container {
    background-color: rgba(240, 37, 22, 0.1);
}

.cell-container {
    background-color: rgba(255, 38, 255, 0.1);
}
</style>
