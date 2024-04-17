---
layout: default
title: Home
---
{% for post in site.posts %}

<article class="flex flex-col shadow my-4">
    <!-- Article Image -->
    <a href="{{ post.url }}" class="hover:opacity-75">
        <img src="https://source.unsplash.com/collection/1346951/1000x500?sig=1">
    </a>
    <div class="bg-white flex flex-col justify-start p-6">
        <a href="#" class="text-blue-700 text-sm font-bold uppercase pb-4">{{ post.category }}</a>
        <a href="#" class="text-3xl font-bold hover:text-gray-700 pb-4">{{ post.title }}</a>
        <p href="#" class="text-sm pb-3">
            By <a href="#" class="font-semibold hover:text-gray-800">{{post.author}}</a>, Published on {{ post.date | date_to_string }}
        </p>
        <a href="#" class="pb-6">{{ post.excerpt }}</a>
        <a href="{{ post.url }}" class="uppercase text-gray-800 hover:text-black">Continue Reading <i class="fas fa-arrow-right"></i></a>
    </div>
</article>

{% endfor %}