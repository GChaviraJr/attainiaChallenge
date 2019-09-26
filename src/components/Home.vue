<template id="gradient">
  <div>
    <h1>Welcome to the Challenge!</h1>
    <p class="p1">
        Please click on a link above to get started!
    </p>
    <p class="p2">
        This is a coding challenge where I have a json file of data and 
        I dynamically add that info into a table on two separate pages. 
        I then highlight a row where the login count is either 0 or greater
        than or equal to 1. 
    </p>
  </div>
</template>
<script>

export default {
  name: 'Home'
}
</script>

<style>
h1 {
    font-size: 50px;
}
#gradient {
    background: linear-gradient(to right, lightblue)
}
header {
    font-size: 40px;
}
.p1 {
    font-size: 30px;
}
.p2 {
    font-size: 20px;
}
</style>
