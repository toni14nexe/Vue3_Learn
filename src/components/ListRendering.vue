<template>
    <div>

        <li v-for="car in cars">
            {{ car.color }}
        </li>
        <br><br>
        <li v-for="(car, index) in cars">
            {{index}} - {{ car.color }}
        </li>
        <br><br>
        <li v-for="(edition, index) in editions">
            {{editions[index]}}
        </li>

    </div>
</template>

<script>
export default {
    data(){
        return{
            cars: [
                { color: 'black' }, 
                { color: 'white' },
                { color: 'red' }, 
                { color: 'gray' }
            ],
            editions: [
                        'Stock',
                        'Highline',
                        'GTD',
                        'GTI',
                        'R-line'
                    ]
        }
    }
}
</script>

<style>

</style>