<script setup>
    import { useRouter } from "vue-router";

    const router = useRouter();
    const {blog} = defineProps(["blog"]);

    function detailView(id) {
        router.push(`/blogs/${id}`);
    }
</script>

<template>
    <div class="itemBox" @click="detailView(blog.id)">{{ blog.title }}
    </div>
</template>

<style scoped>

.itemBox {
    width: 100%;
    cursor: pointer;
    display: flex;
    justify-content:center;
    border: 1px solid;
    align-items: center;
    text-align: center;
    height: 30px;
    margin: 1%;
}

label {
    margin-left: 1%;
}

button {
    margin-right: 1%;
}
</style>