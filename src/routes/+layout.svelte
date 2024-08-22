<script lang="ts">
  import "../app.css";
</script>

<div class="min-h-screen flex flex-col">
  <header class="bg-white shadow-md">
    <nav class="container mx-auto px-4 py-6 flex justify-between items-center">
      <a href="/" class="text-2xl font-bold text-gray-800">FLUIDEFORM 
      <br>Surf + Pilates</a>
      <ul class="flex space-x-6">
        <li><a href="/" class="text-gray-600 hover:text-gray-800">Home</a></li>
        <li><a href="/about" class="text-gray-600 hover:text-gray-800">About</a></li>
        <li><a href="/classes" class="text-gray-600 hover:text-gray-800">Classes</a></li>
        <li><a href="/instructors" class="text-gray-600 hover:text-gray-800">Instructors</a></li>
        <li><a href="/contact" class="text-gray-600 hover:text-gray-800">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main class="flex-grow container mx-auto px-4 py-8">
    <slot />
  </main>

  <footer class="bg-gray-800 text-white">
    <div class="container mx-auto px-4 py-6 flex justify-between items-center">
      <p>&copy; 2024 FLUIDEFORM Surf + Pilates. All rights reserved.</p>
      <nav>
        <ul class="flex space-x-4">
          <li><a href="#" class="hover:text-gray-300">Privacy Policy</a></li>
          <li><a href="#" class="hover:text-gray-300">Terms of Service</a></li>
        </ul>
      </nav>
    </div>
  </footer>
</div>