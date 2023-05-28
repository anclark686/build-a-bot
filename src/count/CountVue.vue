<template>
    Count: {{ count }}
    <button @click="increment()">Increment Count</button>
</template>

<script>
import { ref } from 'vue';
export default {
    setup(props) {
        let count = ref(0)

        const increment = () => count.value = count.value + 1;

        return {
            count,
            increment,
        }
    }
}
</script>