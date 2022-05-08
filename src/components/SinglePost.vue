<!---WARNING: DEPRECATED--->

<template>
    <div class='post'>
        <h3>{{ post.title }}</h3>
        <p>{{ post.body }}</p>
    </div>
</template>

<script>
export default {
    props: ['post'],
}
</script>

<style>
.post {
    background: #acb3d8;
    margin: 20px 10% 20px 10%;
    padding: 5px;
    border-radius: 10px;

    text-align: left;
}

.post h3 {
    padding: 0;
}
</style>