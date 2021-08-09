<template>
    <div>
        <LikeHeader>
            <h3>c</h3>
            <template v-slot:title>
                <h1>こんにちは</h1>
            </template>
            <h3>a</h3>
            <h3>b</h3>
            <template v-slot:number>
                <p>{{ number }}</p>
            </template>
        </LikeHeader>
        <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
        <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    </div>
</template>

<script>
import LikeHeader from './components/LikeHeader.vue'
export default {
    data() {
        return {
            number: 10,
        }
    },
    components: {
        LikeHeader: LikeHeader,
    },
    methods: {
        incrementNumber(value) {
            this.number = value;
        }
    }
}
</script>

<style scoped>
    div {
        border: 1px solid blue;
    }
</style>