<template>
    <div>
       <button @click="send_user">{{user[`name`]}}</button>
    </div>
</template>

<script>
    export default {
        props:{
            user: Object
        },
        methods: {
            send_user() {
                    this.$emit(`user_clicked`, this.user);
                
            }
        },
    }
</script>

<style scoped>

</style>