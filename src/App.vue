<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent = 'appBlue'">Load Blue Template</button>
                <button class="btn btn-success" @click="selectedComponent = 'appGreen'">Load Green Template</button>
                <button class="btn btn-danger" @click="selectedComponent = 'appRed'">Load Red Template</button>
                <hr>
                <component :is="selectedComponent">
                    <p>This is default</p>
                </component>
                <!-- <app-blue>
                    <h1>Blue moon</h1>
                    <p>What rhymes with blue?</p>
                    <input type="text" name="blueanswer">
                </app-blue>
                <app-green>
                    <h1>Green moon</h1>
                    <p>I don't like green</p>
                </app-green>
                <app-red>
                    <h1>Red moon</h1>
                    <p>Is this your favorite color</p>
                    <input type="text" name="redanswer">
                </app-red> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        },
        data: function () {
            return {
                selectedComponent: 'appBlue'
            }
        }
    }
</script>

<style>
</style>