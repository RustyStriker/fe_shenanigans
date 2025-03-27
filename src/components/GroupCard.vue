<script lang="ts">
export default {
    props: {
        title: String,
        imageUrl: String,
        cost: String,
        date: String,
    }
}
</script>
<template>
    <div class="glowHover"
        style="display: flex; flex-direction: column; background-color: #9090fc; padding: 0px; border-radius: 8px; margin: 8px;">
        <h3 style="align-self: center;">{{ title }}</h3>
        <img :src="imageUrl" width="512">
        <div style="flex-grow: 1"></div>
        <div style="display: flex; padding: 0px 8px;">
            <p style="flex-grow: 1;">{{ cost }}</p>
            <p>{{ date }}</p>
        </div>
    </div>

</template>
<style scoped>
.glowHover {
    transition: box-shadow 0.5s ease-out;
}

.glowHover:hover {
    box-shadow: 4px 4px 8px blue;
}
</style>