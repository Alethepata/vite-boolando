<script>
export default {
    name: 'Menu',
    props: {
        type: String,
        link: String
    }

}
</script>

<template>

            <li><a :href="link">{{type}}</a></li>
  
</template>

<style>

</style>