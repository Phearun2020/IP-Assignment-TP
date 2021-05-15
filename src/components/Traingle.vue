<template>
    <div id="traingle" :style="{'--color':color}"></div>
</template>

<script>
    export default {
        name: 'Traingle',
        props: ['color'],
    }
</script>

<style scoped>
:root {
    --color: red
}
#triangle{
  margin-left: 40px;
  width: 0;
  height: 0;
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  border-bottom: 50px solid var(--color);
  margin-top: 2%;
}
</style>