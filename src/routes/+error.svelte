    
    <script>
      import { page } from '$app/stores';
    </script>
    
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100">
      <h1 class="text-4xl font-bold text-gray-800 mb-4">
        {$page.status}: {$page.error?.message}
      </h1>
      <p class="text-gray-600 mb-8">
        Sorry, something went wrong. Please try again later.
      </p>
      <a
        href="/"
        class="px-6 py-3 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors"
      >
        Go back home
      </a>
    </div>
    