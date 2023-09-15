<template>
    <div>
        <h1>{{ count }}</h1>
    </div>
</template>

<script>
    export default{
        props: {
            initialValue: {
                required: true,
                type: Number,
                default: 10,
                description: "Initial value of counter"
            },
            delay: {
                default: 1000
            }
        },
        data(){
            return {
                count: 100
            }
        },
        mounted(){
            this.count = this.initialValue;
            this.startCountDown();
        },
        methods: {
            startCountDown(){
                setTimeout(() => {
                    this.count--;
                    this.startCountDown();
                }, this.delay);
            }
        }
    }
</script>
