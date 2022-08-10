<template>
    <div>
        <h1>Reactivity Component</h1>
        <br>
        <h3>Counter</h3>
        <button @click="increment">{{counter}}</button>
        <br><br>
        <h3>Cars</h3>
        <p class="inline">More than 4 types of color: </p>
        <span class="inline">{{ car.colors.length > 4 ? 'YES' : 'NO' }}</span>
        <br>
        <p class="inline">More than 4 types of editions: {{numberOfEditions}}</p>
        <br><br>
        <h3 class="inline">Page entered at: </h3>
        <p class="inline">{{timeNow()}}</p>
        <br><br>
        <h3>Get & Set - test</h3>
        <p>{{getMe('Toni', 'Kolarić')}}</p>
        <p>{{getMeComputed}}</p>
        <br><br>
        <h3>Playing with component printing</h3>
        <p>{{car.name}}</p>
        <p>{{car.colors[1]}}</p>
        <br><br>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                counter: 0,
                car: {
                    name: 'Golf VIII',
                    colors: [
                    'Black',
                    'White',
                    'Gray',
                    'Red'
                    ],
                    editions: [
                        'Stock',
                        'Highline',
                        'GTD',
                        'GTI',
                        'R-line'
                    ],
                },
                name: 'Toni',
                surname: 'Kolarić',
                age: 23
            }
        },
        methods: {
            increment() {
                this.counter++
            },
            timeNow() {
                const current = new Date();
                const date = current.getDate()+'.'+(current.getMonth()+1)+'.'+current.getFullYear()+'.';
                const time = current.getHours() + ":" + current.getMinutes() + ":" + current.getSeconds();
                const dateTime = date +' '+ time;
                return dateTime;
            },
            getMe(name, surname){
                return name+' '+surname+', '+this.age
            }
        },
        computed:{
            numberOfEditions(){
                return this.car.editions.length > 4 ? 'YES' : 'NO';
            },
            getMeComputed(){
                return this.name+' '+this.surname+', '+this.age;
            }
        }
    }
</script>

<style scoped>
    .inline{
        display: inline;
    }
</style>