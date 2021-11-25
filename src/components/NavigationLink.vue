<template>
    <a :href="url" class="nav-link">
        <slot name="image">
            Kein Bild definiert </slot>|
        <slot></slot>
        ➡
    </a>
</template>

<script>

export default {
    props:['url'],
     name: "NavigationLink"
}
</script>
<style>
a:link, a:active, a:visited, a:hover{
    color: #f00;
}
</style>
