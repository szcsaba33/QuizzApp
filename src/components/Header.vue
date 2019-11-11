<template>
    <div>
        <b-nav tabs>
            <b-nav-item disabled><b>Quiz App</b></b-nav-item>
            <b-nav-item disabled>Counter: {{numCorrect}}/{{numTotal}} </b-nav-item>
            <b-nav-item disabled>Number of Questions: {{amount}}</b-nav-item>
            <li v-for="i in optionsCat" v-bind:key="{ value: i.value, text: i.text }">
                <b-nav-item disabled v-if="i.value === selectedCategory">Selected Category: {{i.text}}</b-nav-item>
            </li>
            <li disabled v-for="i in optionsDiff" v-bind:key="{ value: i.value, text: i.text }">
                <b-nav-item disabled v-if="i.value === selectedDifficulty">Selected Difficulty: {{i.text}}</b-nav-item >
            </li>
            <li v-for="i in optionsType" v-bind:key="{ value: i.value, text: i.text }">
                <b-nav-item disabled v-if="i.value === selectedType">Selected Type: {{i.text}}</b-nav-item>
            </li>


        </b-nav>
    </div>
</template>

<script>
    export default {
        props: [
            'numCorrect',
            'numTotal',
            'amount',
            'selectedCategory',
            'selectedDifficulty',
            'selectedType',
            'optionsCat',
            'optionsDiff',
            'optionsType'
        ],

    }
</script>
