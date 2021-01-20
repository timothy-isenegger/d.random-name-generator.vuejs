<template>
    <div class="name-generator">
        <h2>Select the desired gender</h2>
        <select id="selectGender" @change="updateGender">
            <option value="0">Male</option>
            <option value="1">Female</option>
        </select>

        <h2>Select the desired race</h2>
        <select id="selectRace" @change="updateRace">
            <option value="0">Human</option>
            <option value="1">Elf</option>
        </select>

        <div>
            <button id="buttonGenerate" @click="generateName" class="btn btn-primary">Generate now</button>
        </div>
        <h2>Your generated name is</h2>
        <span class="firstname">{{ firstname }}</span>&nbsp;<span class="lastname">{{ lastname }}</span> 
    </div>
</template>

<script>
export default {
    name: 'NameGenerator',
    data () {
        return {
            firstname: '',
            lastname: '',
            randomNumber: 1,
            gender: 0,
            race: 0,
            firstnames: [
                {
                    male: [
                        {
                            human: [
                                'Tim',
                                'Lukas'
                            ]
                        }
                    ]
                },
                {
                    female: [
                        {
                            human: [
                                'Corinne',
                                'Yvonne'
                            ]
                        }
                    ]
                }
            ],
            lastnames: [
                {
                    male: [
                        {
                            human: [
                                'Isenegger',
                                'Fischer'
                            ]
                        }
                    ]
                },
                {
                    female: [
                        {
                            human: [
                                'Kardashian',
                                'Tripulin'
                            ]
                        }
                    ]
                }
            ]
        }
    },
    methods: {
        generateName() {
            this.firstname = this.firstnames[this.currentGender][this.currentRace][this.randomNumber];
            this.lastname = this.lastnames[this.currentGender][this.currentRace][this.randomNumber];
        },
        updateGender() {
            this.gender = document.getElementById('selectGender').value;
        },
        updateRace() {
            this.race = document.getElementById('selectRace').value;
        }
    }
}
</script>

<style scoped>
    .name-generator {
        text-align: left;
    }
</style>

