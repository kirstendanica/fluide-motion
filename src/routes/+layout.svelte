<script lang="ts">
  import "../app.css";
    import Logo from '$lib/Logo.svelte';
</script>

<div class="min-h-screen flex flex-col">
  <header class="bg-ocean-100 shadow-md fixed w-full z-10">
  <nav class="container mx-auto px-4 py-6 flex justify-between items-center">
    <a href="#home" class="text-2xl font-bold text-ocean-800">
      <Logo width="150" height="40" />
  <ul class="flex space-x-6">
    <li><a href="#home" class="text-gray-600 hover:text-gray-800">Home</a></li>
    <li><a href="#about" class="text-gray-600 hover:text-gray-800">About</a></li>
    <li><a href="#classes" class="text-gray-600 hover:text-gray-800">Classes</a></li>
    <li><a href="#contact" class="text-gray-600 hover:text-gray-800">Contact</a></li>
  </ul>
</nav>
  </header>

  <main class="flex-grow container mx-auto px-4 py-8">
    <slot />
  </main>

  <footer class="bg-ocean-800 text-white py-8">
  <div class="container mx-auto px-4 text-center">
    <p>&copy; 2024 Fluid M/Ocean. All rights reserved.</p>
      <nav>
        <ul class="flex space-x-4">
          <li><a href="#" class="hover:text-gray-300">Privacy Policy</a></li>
          <li><a href="#" class="hover:text-gray-300">Terms of Service</a></li>
        </ul>
      </nav>
    </div>
  </footer>
</div>