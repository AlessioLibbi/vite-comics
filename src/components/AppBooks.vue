<script>
export default {
    name: "AppBooks",
    props: {
        immage: String,
        prezzo: String,
        serie: String,
        tipo: String
    }
}

</script>

<template>
    <div class="card">
        <img :src="immage">
        <p>{{ serie }}</p>
        <p>{{ prezzo }}</p>
    </div>
</template>

<style scoped lang="scss">
.card {
    width: calc(100% / 6 - 20px);
    height: 400px;

    img {
        height: 80%;
        width: 100%;
    }

    p {
        color: white;

    }

    &:hover {
        opacity: 0.5;

    }
}
</style>