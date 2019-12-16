<template>
    <b-navbar :class="{'boxshadow' : scrolled}" fixed="top" type="dark" variant="secondary">
        <b-navbar-brand href="#" class="w-100">To-Do-List</b-navbar-brand>
    </b-navbar>
</template>

<script>
export default {
    data () {
        return {
            scrolled: false
        };
    },

    created () {
        window.addEventListener('scroll', this.handleScroll);
    },
    
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },

    methods: {
        handleScroll () {
            this.scrolled = window.scrollY > 0;
        }
    },

}
</script>

<style>
    .boxshadow{
        box-shadow: 0px 5px 15px 0px rgba(0,0,0,0.75);
    }
</style>