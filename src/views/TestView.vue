<template>
    <div class="test">
        <h1>Test</h1>
        <div v-for="test in tests" :key="test.id">
            <router-link :to="`/test/${test.id}`">
                {{ test.title }}
            </router-link>
        </div>
    </div>
</template>
<script>
export default {
  data(){
    return {
      tests: [
                {
                    id: 1,
                    title: 'Test1'
                },
                {
                    id: 2,
                    title: 'Test2'
                }
            ]
        }
    }
}
</script>