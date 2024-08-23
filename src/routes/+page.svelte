<script lang="ts">
  import { onMount } from 'svelte';

  onMount(() => {
    const smoothScroll = (target: string) => {
      document.querySelector(target).scrollIntoView({
        behavior: 'smooth'
      });
    };

    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        smoothScroll(this.getAttribute('href'));
      });
    });
  });
</script>

<svelte:head>
  <title>FLUIDEFORM Surf + Pilates - Discover Your Strength</title>
</svelte:head>

<section id="home" class="text-center py-20 bg-gray-100">
  <h1 class="text-4xl font-bold mb-4">Welcome to FLUIDEFORM</h1>
  <p class="text-xl mb-8">Discover your strength. Ignite your balance.</p>
  <a href="#classes" class="bg-blue-500 text-white px-6 py-3 rounded-lg hover:bg-blue-600 transition duration-300">
    Explore Our Classes
  </a>
</section>

<section id="about" class="py-20">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold mb-8 text-center">About FLUIDEFORM</h2>
    <p class="text-xl mb-8 text-center">
      FLUIDEFORM Surf + Pilates is where strength meets the waves. We combine the core-strengthening power of Pilates with the balance and agility needed for surfing.
    </p>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <div>
        <h3 class="text-2xl font-semibold mb-4">Our Mission</h3>
        <p>To create a community of strong, balanced individuals who thrive both on land and in the water.</p>
      </div>
      <div>
        <h3 class="text-2xl font-semibold mb-4">Our Approach</h3>
        <p>We blend traditional Pilates techniques with surf-inspired movements to create a unique, effective workout experience.</p>
      </div>
    </div>
  </div>
</section>

<section id="classes" class="py-20 bg-gray-100">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold mb-8 text-center">Our Classes</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div class="bg-white p-6 rounded-lg shadow-md">
        <h3 class="text-2xl font-semibold mb-4">Surf Pilates</h3>
        <p>Combine Pilates with surf-inspired movements to boost your performance on the waves.</p>
      </div>
      <div class="bg-white p-6 rounded-lg shadow-md">
        <h3 class="text-2xl font-semibold mb-4">Core Flow</h3>
        <p>Focus on building core strength and flexibility with this dynamic Pilates flow.</p>
      </div>
      <div class="bg-white p-6 rounded-lg shadow-md">
        <h3 class="text-2xl font-semibold mb-4">Beach HIIT</h3>
        <p>High-intensity interval training on the beach to improve cardiovascular fitness and strength.</p>
      </div>
    </div>
  </div>
</section>

<section id="contact" class="py-20">
  <div class="container mx-auto px-4">
    <h2 class="text-3xl font-bold mb-8 text-center">Contact Us</h2>
    <form class="max-w-lg mx-auto">
      <div class="mb-4">
        <label for="name" class="block mb-2">Name</label>
        <input type="text" id="name" class="w-full p-2 border rounded" required>
      </div>
      <div class="mb-4">
        <label for="email" class="block mb-2">Email</label>
        <input type="email" id="email" class="w-full p-2 border rounded" required>
      </div>
      <div class="mb-4">
        <label for="message" class="block mb-2">Message</label>
        <textarea id="message" class="w-full p-2 border rounded" rows="4" required></textarea>
      </div>
      <button type="submit" class="bg-blue-500 text-white px-6 py-3 rounded-lg hover:bg-blue-600 transition duration-300">Send Message</button>
    </form>
  </div>
</section>