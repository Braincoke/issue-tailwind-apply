<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

    <h1>Hello, world!</h1>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
    </p>

    <p class="home-links">
      <a href="https://gridsome.org/docs/" target="_blank" rel="noopener">Gridsome Docs</a>
      <a href="https://github.com/gridsome/gridsome" target="_blank" rel="noopener">GitHub</a>
    </p>

    <div class="bg-gray-400 mt-5 py-10 px-4 rounded text-green-800">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
        Rem dolor perspiciatis officia? Obcaecati quae harum asperiores,
        praesentium quasi alias qui.</p>
    </div>
    <div class="text-yellow-700">
      This text is yellow.
      <a href="#">This is a link</a>
    </div>
    <a href="#" class="text-purple-700">This link should be purple</a>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
