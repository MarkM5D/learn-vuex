<template>
    <div>
        <input placeholder="Enter color name" type="text" v-model="colorCode">
    </div>
</template>

<script>
export default {
    computed: {
        colorCode: {
            get() {
                return this.$store.state.colorCode
            },
            set(newValue) {
                return this.$store.dispatch('setColorCode', newValue)
            }
        }
    },
}
</script>

<style></style>