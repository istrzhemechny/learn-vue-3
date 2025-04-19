<template>
    <div class="blog-posts-layout">
        <aside class="blog-post-list">
            <BlogPostList></BlogPostList>
        </aside>
        <main class="blog-post-content-with-sidebar"> 
            <Router-view class="blog-post-content"></Router-view>
            <Router-view name="sidebar"></Router-view>
        </main>
    </div>
</template>

<script setup>
import BlogPostList from '@/components/BlogPostList.vue';

</script>

<style lang="scss" scoped>
.blog-posts-layout{
    display: flex;
    gap: 1rem;
    width: 100%;
    .blog-post-list {
        flex: 0 0 25%;
    }
    .blog-post-content-with-sidebar{
        display: flex;
        flex: 0 0 75%;

        .blog-post-content {
            flex: 1;
        }
    }
}
</style>