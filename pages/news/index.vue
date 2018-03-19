<template>
    <div>
        <h2>News Index page</h2>
        <p>NewsID: {{ $route.params.newsId }}</p>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/news/123">News-1</a></li>
            <li><nuxt-link :to="{name: 'news-id', params: {id: 456, title: 'liuxiang57.com'}}">News-2</nuxt-link></li>
        </ul>
    </div>
</template>