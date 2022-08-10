<template>
    <div>

        <!-- if state -->
        <button @click="awesome1 = !awesome1">if state</button>
        <h1 v-if="awesome1">Vue is awesome!</h1><br><br>

        <!-- if-else state -->
        <button @click="awesome = !awesome">if-else state</button>
        <h1 v-if="awesome">Vue is awesome!</h1>
        <h1 v-else>Oh no</h1><br><br>

        <!-- if-else if-else state -->
        <button @click="strFunction()">if-else if-else state</button>
        <div v-if="Str == ''">
            <h1>Empty string Str</h1>
        </div>
        <div v-else-if="Str == 'A'">
            <h1>Str is 'A'</h1>
        </div>
        <div v-else-if="Str === 'a'">
            <h1>Str is 'a'</h1>
        </div>
        <div v-else>
            <h1>Str is not empty, it is '{{Str}}'</h1>
        </div><br><br>

        <!-- if on template -->
        <button @click="ok = !ok">if template state</button>
        <template v-if="ok">
            <h1>if on template</h1>
            <p>Paragraph</p>
        </template><br><br>

        <!-- if on template -->
        <button @click="ok1 = !ok1">if template state</button>
        <h1 v-show="ok1">Hello!</h1>

    </div>
</template>

<script>
export default {
    data(){
        return{
            awesome1: true,
            awesome: false,
            Str: '',
            ok: true,
            ok1: true
        }
    },
    methods:{
        strFunction(){
            if(this.Str == ''){ this.Str = 'A' }
            else if(this.Str == 'A'){ this.Str = 'a' }
            else if(this.Str == 'a'){ this.Str = 'B' }
            else if(this.Str == 'B'){ this.Str = '' }
        }
    }
}
</script>

<style>
</style>