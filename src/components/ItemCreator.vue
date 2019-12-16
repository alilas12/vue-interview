<template>
    <b-container fluid>
        
        <b-form-group class="w-100" type="text">
            <b-col cols="8" class="float-left pl-0">
                <b-form-input  @keyup.enter.native="AddItem" v-model="newInput"></b-form-input>
            </b-col>
            <b-col cols="4" class="float-left p-0 w-100">
                <b-button class="w-100" :disabled="newInput === ''" @click="AddItem" variant="success">Add</b-button>
            </b-col>
        </b-form-group>

    </b-container>
</template>

<script>
export default {
    name: 'itemcreator',
    data() {
        return {
            newInput: this.input,
        }
    },
    
    props: {
        items: {
            type: Array
        },
        input: {
            type: String,
            required: true,
        }
    },

    methods: {
        AddItem() {
            const sha256 = require('js-sha256');
            const hash = sha256(this.newInput);
            this.items.push(hash);
        },
    },
}
</script>