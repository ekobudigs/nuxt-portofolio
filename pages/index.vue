<script setup>
    const { data: posts } = await useAsyncData('latest-posts', () =>
    queryContent('/blog')
    .sort({data: 1})
    .limit(3)
    .find()
    )
</script>

<template>
    <section>
        <h1 class="text-5xl font-bold mt-20">👋🏻 Hello, I'm Eko Budi!</h1>
    <p class="text-base text-gray-900 p-2 italic">Fullstack Developer</p>
    </section>

    <section class="flex flex-col md:flex-row">
        
        <div class="md:w-3/4">
            <h2 class="text-3xl font-bold mt-8">My Story</h2>
        <p class="text-lg py-2">
            I am a Laravel Developer with 11 months of work experience. My skills include PHP, Javascript, HTML, CSS, JQUERY, SQL, and Cloud Computing. I have also completed the Google IT Support course. During my work experience, I have successfully completed various projects using these technologies
        </p>
        <p class="text-lg py-2">
            I have the ability to adapt quickly in a dynamic work environment, and I highly value teamwork and collaboration. I have a high level of perseverance and commitment to solving problems and providing the best solutions for clients. I am also proficient in delivering technical support to users efficiently
        </p>
        <p class="text-lg py-2">
            I enjoy working in a collaborative team environment, where I can learn from my colleagues and share knowledge. I am motivated to continuously learn and develop my skills in this industry. I believe that the combination of my work experience, technical expertise, and interpersonal skills make me a suitable candidate for the position of IT Support Developer. I am ready to provide valuable contributions to your team. Thank you for your attention. I look forward to further discussing how I can assist your team in achieving their goals.
        </p>
    </div>

    <img src="~/assets/images/eko1.png" class="w-1/2 md:max-w-sm p-8 mx-auto" /> 
    </section>

    <section>
        <h2 class="text-3xl font-bold mt-8">Latest Blog Post</h2>
        <div class="grid md:grid-cols-3 pt-8 gap-10">
            <Post :posts="posts" />
        </div>
    </section>
</template>