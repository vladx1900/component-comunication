<template>
    <div class="container">
        <div class="col-xs-12">
            <h3>Hello , i'm the PARENT!</h3>
            <p>My Name Is: {{name}}</p>
            <button @click="changeName">Change Name</button>
            <hr>
        </div>
        <div class="row">
            <app-firstChild
                    :name="name"
                    @nameWasChanged="name = $event"
            ></app-firstChild>
            <app-second-child
                    :name="name"
                    @changeName="name = $event"
            ></app-second-child>
        </div>
    </div>
</template>

<script>
    import FirstChild from './FirstChild.vue';
    import SecondChild from './SecondChild.vue';

    export default {
        data: function () {
            return {
                name: 'Mike'
            }
        },
        components: {
            appFirstChild: FirstChild,
            appSecondChild: SecondChild
        },
        methods: {
            changeName: function () {
                this.name = "Carl";
            }
        }
    }
</script>