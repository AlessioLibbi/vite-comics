<script>
export default {
    name: "AppContent"
}
</script>

<template>
    <div class="content-box">

        <div class="content-container">
            <h2>-->Content Here &lt;--</h2>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.content-box {
    background-color: $text-color;

    .content-container {
        @include flex(row, flex-start, center);
        margin: 0 auto;
        height: 140px;
        width: $width;

        h2 {
            color: white;
        }
    }

}
</style>