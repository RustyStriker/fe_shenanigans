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
        style="display: flex; flex-direction: column; background-color: #d7e8ba; padding: 0px; border-radius: 8px; margin: 8px;">
        <div style=" display: flex; flex-direction: column; border-radius: 8px 8px 0px 0px;">
            <h3 style="align-self: center;">{{ title }}</h3>

        </div>
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
    box-shadow: 0px 0px 16px #ffa630;
}
</style>