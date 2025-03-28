<script lang="ts">

export default {
    props: {
        title: String,
    }
}

</script>

<template>
    <div style="width:100%; margin: auto; display: flex; flex-direction: row; color: black; background-color: #fca9a9">
        <div class="hovermenu" style="margin: 8px 16px; display: flex;">
            <img src="../assets/logo.svg" height="32px" style="align-self: center;" />
            <div class="menu" style="width:max-content; padding-right: 8px;">
                <ul>
                    <li><button>Button 1</button></li>
                    <li><button>Button 2</button></li>
                    <li><button>Ok you get the idea</button></li>
                </ul>
            </div>
        </div>
        <p>Very Cool Flight Planner: {{ title ?? 'TITLE MISSING WTF' }}</p>
    </div>
</template>
<style scoped>
div {
    border-radius: 8px;
}

.menu {
    display: none;
    position: absolute;
    top: 100%;
    background-color: #a9fc9a;
}

.hovermenu {
    position: relative;
}

.hovermenu:hover .menu {
    display: flex;
}

.menu button {
    background-color: #ffffff30;
    border-color: #00000020;
    border-radius: 8px;
    padding: 2px 8px;
}
</style>