<template>
    <div class="name-generator">
        <h2>Select the desired gender</h2>
        <select id="selectGender">
            <option value="male">Male</option>
            <option value="female">Female</option>
        </select>

        <h2>Select the desired race</h2>
        <select id="selectRace">
            <option value="human">Human</option>
            <option value="elf">Elf</option>
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
            firstnames: [
                'Tim',
                'Lukas',
            ],
            lastnames: [
                'Isenegger',
                'Fischer',
            ]
        }
    },
    computed: {
        currentGender() {
            return document.getElementById('selectGender').value;
        },
        currentRace() {
            return document.getElementById('selectRace').value;
        }
    },
    methods: {
        generateName() {
            this.firstname = this.firstnames[0];
            this.lastname = this.lastnames[1];
        }
    }
}
</script>

<style scoped>
    .name-generator {
        text-align: left;
    }
</style>

