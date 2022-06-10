<template>
    <div class="test">
        <h1>Test</h1>
        <div>{{ test.title }}</div>
    </div>
</template>
<script>
export default {
    props: {
        id: {
            type: String,
            required: true,
        }
    },
    data() {
        return {
            tests: [
                {
                    id:1,
                    title: 'Test1'
                },
                {
                    id:2,
                    title: 'Test2'
                }
            ]
        }
    },
     computed: {
        test(){
            return this.tests.find(test => test.id == this.id)
            }
        },
  mounted(){
    console.log(this.$route)
  }
}
</script>