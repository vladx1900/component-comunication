<template>
    <div class="col-xs-6">
        <h4>Hello, i'm the first child!</h4>
        <p>My Parent Name Is: {{name}}</p>
        <button @click="changeName">Change Name</button>
    </div>
</template>

<script>

    export default {
        props: ['name'],
        methods: {
            changeName: function () {
                this.name = "Carl_Child";
                this.$emit('nameWasChanged', this.name);
            }
        }
    }
</script>