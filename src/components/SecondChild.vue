<template>
    <div class="col-xs-6">
        <h4>Hello, i'm the second child!</h4>
        <p>My Parent Name Is: {{name}}</p>
        <button @click="changeName">Change Name</button>
    </div>
</template>

<script>

    export default {
        props: ['name'],
        methods: {
            changeName: function () {
                this.name = "Second_Carl";
                this.$emit('changeName', this.name);
            }
        }
    }
</script>